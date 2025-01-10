Can I use MultilingualPress in a single-site WordPress installation?

You cannot use MultilingualPress in a single-site WordPress installation. For MultilingualPress you need to have a [WordPress multisite installation](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/).

## Explanation in Detail: Why you can use MultilingualPress only in a WordPress multisite installation

To enable the use of MultilingualPress for a single site, we would have to interfere with the way WordPress saves content. However, there are plugins that accomplish exactly that. But we think this is a bad idea. After deactivating the plugin, you would lose access to your translated content.

The entire concept of MultilingualPress is based on using **a corresponding site for each language** (in the WordPress network, this means a multisite). Links between sites and between translated content (e.g. posts or terms) are saved in separate plugin tables. This makes it possible for the individual sites only to store the actual **non-manipulated content**, that is, **without injected shortcode**, as is (necessarily) the case for some single-site plugins.

If you currently have a single-site installation, you can change this to a multisite. You can find detailed instructions for this [here.](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/)