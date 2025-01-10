To get an array of connected posts you can use the `translationIds` function. That method is the equivalent of `mlp_get_linked_elements` in MultilingualPress 2:

The first parameter is the **source post id**, the second is the column "**type**" in the wp_mlp_relationships table in the database and the third parameter is the **source site id**.

About the type value, it must be designated as "post," "term," or "comment" to query the translation of a post, term, or comment respectively.

$translations = \Inpsyde\MultilingualPress\translationIds(1, 'post', 1);

it will return an array of key value pairs as site id and post id:

array (size=2)

1 => int 1

2 => int 1

You can loop through `$translations` like this:

if($translations) {

   foreach($translations as $siteId => $postId) {
      echo 'Site ID: ' . $siteId . ' Post ID: ' . $postId . '<br>';
   }
}