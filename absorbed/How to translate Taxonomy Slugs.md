In this brief tutorial we show how to translate taxonomy slugs using the _multilingualpress.filter_term_public_url_ filter hook available in MultilingualPress.

### Set the environment for our example code snippet

Here below we provide an example snippet with two sub sites that have respectively an ID with value 1, and a second one with value 2.  
Of course this example uses two sites, but you can extend it: the ID values can be more, and in any case have to be properly set depending on the sites configured in your environment.

Besides, in this example we assume that you previously registered the taxonomy _My Taxonomy_ with slug _my-taxonomy-slug_ in the network.

### Implement the snippet for slug translation

In such an environment we can implement the taxonomy slug translation as shown in the filter below.

add_filter(
    'multilingualpress.filter_term_public_url',
    function ($url, $sourceSiteId, $remoteSiteId) {
        $fragments = [
            1 => 'my-taxonomy-slug',
            2 => 'de-my-taxonomy-slug',
        ];

        if (empty($fragments[$sourceSiteId]) || empty($fragments[$remoteSiteId])) {
            return $url;
        }

        return str_replace(
            $fragments[$sourceSiteId],
            $fragments[$remoteSiteId],
            $url
        );
    },
    10,
    3
);

As you can see in the _fragments_ array the proper slug translations are provided for every site. This is a key value pairs array, where keys are site IDs and values are the translated taxonomy slugs. The array elements can be extended depending the number of the sites you have in your Multisite network.

Now, from the MultilingualPress settings, in the _Translatable Taxonomies tab_ enable _My Taxonomy_.

After that, in site with ID 1 create a new _My Taxonomy_ term as _My Term_ and connect it to site with ID 2. The snippet created will properly manage the translations of the slugs when switching between the two sites.