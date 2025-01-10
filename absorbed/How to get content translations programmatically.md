In order to get current content translations of the current post in MultilingualPress, you can use the `Translations` class passing the arguments via `TranslationSearchArgs`. Here is an example:

add_filter('the_content', function($content) {
    $args =
        \Inpsyde\MultilingualPress\Framework\Api\TranslationSearchArgs::forContext(
            new \Inpsyde\MultilingualPress\Framework\WordpressContext()
        )->forSiteId(get_current_blog_id())->includeBase();

    $translations = \Inpsyde\MultilingualPress\resolve(
        \Inpsyde\MultilingualPress\Framework\Api\Translations::class
    )->searchTranslations($args);

    foreach ($translations as $translation) {
        $postId = $translation->remoteContentId();
        $title = $translation->remoteTitle();
        $url = $translation->remoteUrl();

        $language = $translation->language();
        $bcp47tag = $language->bcp47tag();
        $englishName = $language->englishName();
        $isoCode = $language->isoCode();
        $locale = $language->locale();
        $name = $language->name();
    }

    return $content;

});

Now you can loop through the `$translations` array where each `Translation` object contains translation data and language information.