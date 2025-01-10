How to run code when the "Copy source content" option is checked

In this tutorial we are going to show how to run your code snippet when the option _Copy source content_ is selected in the translation metabox.

### The translation metabox

A translation metabox lets you to define some settings related to the post translations that are available in another language sub site.  
When you edit a post you will find the translation metabox right under your content. There will be one metabox for every language site connected through MultilingualPress.

In each metabox it is possible to quickly set some options that affect the post content and configuration in the related language sub site. This way the user can set all the needed options directly in one page.

The option "Copy source content" lets you copy the entire content of the post to the related translation post.

For further information please refer to: [https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/)

### Filter the code and run your snippet

If you need to run some code only when that option is checked, you can use the _multilingualpress.sync_post_meta_keys_ filter.

Here below we provide an example of such implementation.

add_filter('multilingualpress.sync_post_meta_keys', function($keysToSync, $context, $request) {

    $multilingualpress = $request->bodyValue(
        'multilingualpress',
        INPUT_POST,
        FILTER_DEFAULT,
        FILTER_FORCE_ARRAY
    );

    $remoteSiteId = $context->remoteSiteId();
    $translation = $multilingualpress["site-{$remoteSiteId}"] ?? '';

    if(!empty($translation) && $translation['remote-content-copy'] === '1') {
        // Copy source content checked in metabox
    }

    return $keysToSync;
}, 10, 3);

So, here we see that by using the _multilingualpress.sync_post_meta_keys_ filter hook, you can grab from the context the translation metaboxes, and then loop through them.

While looping you can check the status of the related _remote-content-copy_ array key. That value is set accordingly with the _Copy source content_ option.

Finally replace the comment "Copy source content checked in metabox" with your code snippet. This will run when the status is 1.