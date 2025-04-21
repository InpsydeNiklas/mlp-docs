**Purpose**: Demonstrate how to build a fully custom language switcher in WordPress Multisite using MultilingualPress. You’ll learn how to retrieve translations for the current page, display them in a menu or select dropdown, and optionally embed the switcher in a sidebar widget.

---

## 1. Prerequisites

1. **WordPress Multisite** with at least two sites connected by MultilingualPress.
2. **MultilingualPress** (version 3 or 4) installed and network activated.
3. Basic familiarity with **PHP** (for custom code) and optionally **JavaScript** for dropdown events.

---

## 2. Retrieve Translations for the Current Page

MultilingualPress offers a `Translations` service class. To leverage it, we’ll create a helper function:

```php
function multilingualpress_get_translations() {
    // Build arguments for retrieving translations.
    $args = \Inpsyde\MultilingualPress\Framework\Api\TranslationSearchArgs::forContext(
        new \Inpsyde\MultilingualPress\Framework\WordpressContext()
    )
    ->forSiteId(get_current_blog_id())
    ->includeBase();

    // Resolve the Translations service from the container.
    $translations = \Inpsyde\MultilingualPress\resolve(
        \Inpsyde\MultilingualPress\Framework\Api\Translations::class
    )->searchTranslations($args);

    return $translations;
}
```

**What This Does**

- Uses `TranslationSearchArgs` to specify the current site ID and that we should “includeBase” (the current post as well, if needed).
- Returns an **array** of translation objects, each containing data such as `remoteUrl()` (the link to the translated content) and a `language()` object with locale details.

**Testing**

```php
$translations = multilingualpress_get_translations();
foreach ($translations as $translation) {
    $language = $translation->language();
    $isoName  = $language->isoName();    // e.g., "English (US)"
    $locale   = $language->locale();     // e.g., "en_US"
    $url      = $translation->remoteUrl(); 
    // ...
}
```

---

## 3. Insert a Translations Menu Before the Post Content

Let’s create a **simple list-based menu** and prepend it to each single post’s content. We’ll use the `the_content` filter:

```php
add_filter('the_content', function ($content) {
    // Only show the menu on single posts (avoid archives, pages, etc.).
    if (!is_single()) {
        return $content;
    }

    $translations = array_reverse(multilingualpress_get_translations());
    if (!$translations) {
        return $content; // No translations available, return original content.
    }

    $items = '';
    foreach ($translations as $translation) {
        $language = $translation->language();
        $isoName  = $language->isoName();
        $url      = $translation->remoteUrl();

        if ($url) {
            $items .= "<li><a href='{$url}'>{$isoName}</a></li>";
        }
    }

    // Build the menu markup only if we have items.
    if ($items) {
        $menu = "<ul>{$items}</ul>";
        return $menu . $content;
    }

    return $content;
});
```

### Explanation

1. **`is_single()`**: Ensures we only run this on single post pages.
2. **`array_reverse()`**: Reverses the translations array if you want the base language last—change or remove as you prefer.
3. **Generate HTML**: We loop each translation, building `<li>` items linking to `remoteUrl()`.
4. **Append**: We prepend the list to the existing `$content`.

**Result**  
Visitors see a small language list above the post if translations exist (e.g., “English (US), Deutsch, Español”).

---

## 4. Build a `<select>`-Based Language Switcher

Instead of a `<ul>`, let’s display a dropdown that redirects when the user picks a new language. We’ll adapt the snippet:

```php
add_filter('the_content', function ($content) {
    if (!is_single()) {
        return $content;
    }

    $translations = array_reverse(multilingualpress_get_translations());
    if (!$translations) {
        return $content;
    }

    $items = '';
    foreach ($translations as $translation) {
        $language = $translation->language();
        $isoName  = $language->isoName();
        $locale   = $language->locale();
        $url      = $translation->remoteUrl();

        if ($url) {
            $items .= "<option data-url='{$url}' value='{$locale}'>{$isoName}</option>";
        }
    }

    if ($items) {
        $menu  = "<select id='multilingualpress-language-switcher'>";
        $menu .= $items;
        $menu .= "</select>";
        // Simple jQuery to handle selection change and redirect.
        $menu .= "<script>
            jQuery('#multilingualpress-language-switcher').change(function() {
                var selected = jQuery(this).find('option:selected').data('url');
                if (selected) {
                    window.location.href = selected;
                }
            });
        </script>";

        return $menu . $content;
    }

    return $content;
});
```

**Key Points**

- We add a `<select>` element with `<option>` tags for each translation.
- Each option’s `data-url` attribute holds the translation’s `remoteUrl()`.
- The inline `<script>` uses jQuery to watch for selection changes and redirects the browser.

---

## 5. Placing the Switcher in a Widget

If you prefer a switcher in a **sidebar** or **footer** (classic widget areas), register a custom widget:

```php
add_action('widgets_init', function(){
   register_widget('Language_Switcher_Widget');
});

class Language_Switcher_Widget extends WP_Widget {

   public function __construct() {
      $widget_ops = [
         'classname'   => 'language_switcher',
         'description' => 'Custom MultilingualPress Language Switcher',
      ];
      parent::__construct('language_switcher', 'Language Switcher', $widget_ops);
   }

   public function widget($args, $instance) {
      echo $args['before_widget'];

      $translations = array_reverse(multilingualpress_get_translations());
      if (!$translations) {
         // No translations, no widget output.
         return;
      }

      $items = '';
      foreach ($translations as $translation) {
         $language = $translation->language();
         $isoName  = $language->isoName();
         $locale   = $language->locale();
         $url      = $translation->remoteUrl();

         if ($url) {
            $items .= "<option data-url='{$url}' value='{$locale}'>{$isoName}</option>";
         }
      }

      if ($items) {
         $output  = "<select id='multilingualpress-language-switcher'>";
         $output .= $items;
         $output .= "</select>";
         $output .= "<script>
            jQuery('#multilingualpress-language-switcher').change(function() {
               var selected = jQuery(this).find('option:selected').data('url');
               if (selected) {
                  window.location.href = selected;
               }
            });
         </script>";

         echo $output;
      }

      echo $args['after_widget'];
   }
}
```

### Steps to Use the Widget

1. **Place the Code**: In a custom plugin or your `functions.php`.
2. **Activate**: In WP Admin, go to **Appearance → Widgets** (or block-based widget editor).
3. **Drag/Place**: The “Language Switcher” widget into your desired sidebar/footer.
4. **Save**: The switcher now appears on the front end if translations exist.

---

## Summary & Next Steps

- **You Created a Custom Switcher**: Either as a list of links, a dropdown, or a widget.
- **API Recap**: The `Translations` class + `TranslationSearchArgs` provides direct access to each language site’s remote URL.
- **Styling**: Apply custom CSS or different markup as you see fit.
- **Advanced Customization**:
    - **Flags**: Insert images or icons next to each option using the language’s locale or a separate data source.
    - **Conditionals**: Offer fallback logic if no translation is found for certain languages.
    - **Integration**: Combine with other MultilingualPress features (e.g., Quicklinks or redirection rules) if you need further automation.

By following these steps, you gain full control over **how** and **where** your language switcher appears, ensuring a cohesive multilingual experience tailored exactly to your site’s requirements.


---

## 1. Complete Copy-Paste Example

> **Note**: Save this code in a `.php` file (e.g. `my-mlp-language-switcher.php`) inside your `wp-content/plugins/` directory. Then **Network Activate** (or single-site activate) in your WordPress admin.

```php
<?php
/**
 * Plugin Name: My MLP Language Switcher
 * Description: A custom language switcher for MultilingualPress using a shortcode, with checks for class existence.
 * Version:     1.0
 * Author:      Your Name
 * Text Domain: my-mlp-language-switcher
 *
 * Requires at least: 5.9
 * Requires PHP: 7.4
 */

use Inpsyde\MultilingualPress\Framework\Api\TranslationSearchArgs;
use Inpsyde\MultilingualPress\Framework\WordpressContext;
use Inpsyde\MultilingualPress\Framework\Api\Translations;

/**
 * Check if MultilingualPress classes exist.
 * If they don't, we'll disable the translation code gracefully.
 */
function my_mlp_check_mlp_classes(): bool {
    return class_exists(TranslationSearchArgs::class)
        && class_exists(WordpressContext::class)
        && class_exists(Translations::class)
        && function_exists('Inpsyde\\MultilingualPress\\resolve');
}

/**
 * Helper function to retrieve translations via the MultilingualPress API.
 */
function my_mlp_get_translations(): array {

    // If MLP classes aren't available, return an empty array (no translations).
    if (!my_mlp_check_mlp_classes()) {
        return [];
    }

    // Build arguments for retrieving translations.
    $args = TranslationSearchArgs::forContext(new WordpressContext())
        ->forSiteId(get_current_blog_id())
        ->includeBase();

    // Resolve the Translations service from the container.
    $translationsService = \Inpsyde\MultilingualPress\resolve(Translations::class);
    return $translationsService->searchTranslations($args);
}

/**
 * Create a shortcode [my_language_switcher] to display a select-based switcher.
 */
function my_mlp_language_switcher_shortcode(): string {

    // Retrieve translations (reversed so the current site might appear last; adjust as you wish).
    $translations = array_reverse(my_mlp_get_translations());

    // If no translations or classes not available, display nothing.
    if (!$translations) {
        return '';
    }

    // Build <option> items for each translation.
    $options = '';
    foreach ($translations as $translation) {
        $lang      = $translation->language();
        $isoName   = $lang->isoName();   // e.g. "English (United States)"
        $locale    = $lang->locale();    // e.g. "en_US"
        $remoteUrl = $translation->remoteUrl();

        if ($remoteUrl) {
            $options .= "<option data-url='{$remoteUrl}' value='{$locale}'>{$isoName}</option>";
        }
    }

    // If we have options, build the <select> markup plus a small script to handle redirect.
    if ($options) {
        $output  = "<select id='my-mlp-language-switcher'>";
        $output .= $options;
        $output .= "</select>";
        $output .= "<script>
            (function($){
                $('#my-mlp-language-switcher').change(function() {
                    var selectedUrl = $(this).find('option:selected').data('url');
                    if (selectedUrl) {
                        window.location.href = selectedUrl;
                    }
                });
            })(jQuery);
        </script>";

        return $output;
    }

    return '';
}
add_shortcode('my_language_switcher', 'my_mlp_language_switcher_shortcode');
```

### How It Works

1. **`my_mlp_get_translations()`**: Fetches translations for the current site/post using MultilingualPress’s `Translations` service.
2. **Shortcode**: `[my_language_switcher]`
    - Renders a `<select>` where each `<option>` has a `data-url` pointing to the remote site’s URL for that translation.
    - A small jQuery script listens for changes and redirects the browser to the chosen site’s URL.

---

## 2. Usage in Your Site

1. **Activate the Plugin**
    - Upload the `.php` file into `wp-content/plugins/`, then **Network Activate** or single-site activate it.
2. **Add the Shortcode**
    - In any page/post editor, insert `[my_language_switcher]`.
    - When viewing that page/post, users see a dropdown listing available translations for the current post.
3. **Confirm Linked Translations**
    - Make sure you have connected (linked) the post/page on each language site in MultilingualPress. If no translation exists, it won’t appear in the dropdown.

---

## 3. Customization Tips

- **Styling**: Wrap the `<select>` in additional HTML or add a custom class, then use CSS to style it.
- **Ordering**: Remove `array_reverse()` or implement a custom sorting if you’d prefer alphabetical or locale-based ordering.
- **Flags**: Insert an `<img>` tag or icon in each `<option>` if you want flags or other visual cues.
- **Conditionals**: Only show the switcher for certain post types using `is_singular('custom_post_type')`, etc.

---

## 4. Legacy Note: Widgets

If you need a **sidebar widget** version of this switcher, you can adapt the same logic inside a `WP_Widget` class. However, many newer themes have moved to block-based widget areas. For more on classic widgets, see [WordPress Widget Basics](https://developer.wordpress.org/themes/functionality/widgets/).

_(Most modern sites rely on block patterns or shortcodes inside block areas, so the shortcode approach is typically enough.)_

---

## Summary

By installing this **lightweight plugin**:

- You get a **shortcode** `[my_language_switcher]` that outputs a custom dropdown for each available MultilingualPress translation.
- You control the style, logic, and user experience—without relying on default menus or widgets.

Whether you embed the shortcode in a page, a block, or a custom theme file, you’ll have full flexibility for your site’s multilingual navigation. Enjoy your new **custom language switcher**!