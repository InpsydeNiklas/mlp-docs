In this tutorial we will create a custom language switcher using the MultilingualPress API. We will start creating a simple language menu and then convert it to a select dropdown. Finally we will explain how to add the language switcher to a WordPress widget.

## Get translations for the current page

In order to create a language menu you need a way to get the translations for a particular page. MultilingualPress provides the `Translations` class which accepts search parameter from `TranslationSearchArgs` class like this:

function multilingualpress_get_translations()
{
   $args = \Inpsyde\MultilingualPress\Framework\Api\TranslationSearchArgs::forContext(new \Inpsyde\MultilingualPress\Framework\WordpressContext())
      ->forSiteId(get_current_blog_id())
      ->includeBase();

   $translations = \Inpsyde\MultilingualPress\resolve(
      \Inpsyde\MultilingualPress\Framework\Api\Translations::class
   )->searchTranslations($args);

   return $translations;
}

The above function returns an array of translations, each one containing information like `remote_url` and language info. You can then loop through the array to get the translations:

$translations = multilingualpress_get_translations();

foreach ($translations as $translation) {
   $language = $translation->language();
   $language_iso_name = $language->isoName();
   $language_locale = $language->locale();
   $url = $translation->remoteUrl();
}

## Create a translations menu at the beginning of Post content

Now that we know how to get the translations of a page, we can create a menu. So lets start adding one before the content of the post. To do so we can use the WordPress filter ‘the_content’:

add_filter('the_content', function ($content) {
   if (!is_single()) {
      return $content;
   }

   $translations = array_reverse(multilingualpress_get_translations());

   if (!$translations) {
      return $content;
   }
   
   $output = '';
   $items = '';
   foreach ($translations as $translation) {
      $language = $translation->language();
      $iso_name = $language->isoName();
      $url = $translation->remoteUrl();

      if ($url) {
         $items .= "<li><a href='${url}'>${iso_name}</a></li>";
      }
   }

   if($items) {
      $output .= '<ul>';
      $output .= $items;
      $output .= '</ul>';
   }

   return $output . $content;
});

As you can see at the beginning we return default content in case we are not in a single post page but also in case there are no translations. Then we create the HTML markup for the menu looping through the translations array. Finally we only display the menu in case there are items containing a URL.

## Create a language switcher

We can use part of the previous code but this time we will change the markup to use a select instead of an unordered list:

...

foreach ($translations as $translation) {
   $language = $translation->language();
   $iso_name = $language->isoName();
   $locale = $language->locale();
   $url = $translation->remoteUrl();

   if ($url) {
      $items .= "<option data-url='${url}' value='${locale}'>${iso_name}</option>";
   }
}

if($items) {
   $output .= '<select id="multilingualpress-language-switcher">';
   $output .= $items;
   $output .= '</select>';
   $output .= '<script>';
   $output .= "jQuery('#multilingualpress-language-switcher').change(function() {window.location.replace(jQuery('#multilingualpress-language-switcher option').data('url'));});";
   $output .= '</script>';
}
...

Also we use a bit of JavaScript to fire a page redirect when selector is changed.

## Adding the language switcher to a Widget

Finally the code snippet below shows how to add the above language switcher to a widget:

add_action( 'widgets_init', function(){

   register_widget( 'Language_Switcher_Widget' );

});

class Language_Switcher_Widget extends WP_Widget {

   public function __construct() {
      $widget_ops = array(
         'classname' => 'language_switcher',
         'description' => 'Language Switcher',
      );

      parent::__construct( 'language_switcher', 'Language Switcher', $widget_ops );
   }

   public function widget( $args, $instance ) {
      echo $args['before_widget'];
      $translations = array_reverse(multilingualpress_get_translations());
      if (!$translations) {
         return $content;
      }

      $output = '';
      $items = '';
      foreach ($translations as $translation) {
         $language = $translation->language();
         $iso_name = $language->isoName();
         $locale = $language->locale();
         $url = $translation->remoteUrl();

         if ($url) {
            $items .= "<option data-url='${url}' value='${locale}'>${iso_name}</option>";
         }
      }

      if($items) {
         $output .= '<select id="multilingualpress-language-switcher">';
         $output .= $items;
         $output .= '</select>';
         $output .= '<script>';
         $output .= "jQuery('#multilingualpress-language-switcher').change(function() {window.location.replace(jQuery('#multilingualpress-language-switcher option').data('url'));});";
         $output .= '</script>';
      }

      echo $output;
      echo $args['after_widget'];
   }
}