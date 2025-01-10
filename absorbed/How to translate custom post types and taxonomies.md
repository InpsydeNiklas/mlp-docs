In this document we explain you how to **translate custom post types and taxonomies** in MultilingualPress. To demonstrate it, we'll create a WordPress Multisite installation with two connected sites.

We are going to use the [Custom Post Type UI](https://wordpress.org/plugins/custom-post-type-ui/) plugin to create a custom post type and a taxonomy. Just keep in mind that the process is the same for any other plugin that creates custom post types or if you register them manually using [register_post_type](https://developer.wordpress.org/reference/functions/register_post_type/) and [register_taxonomy](https://developer.wordpress.org/reference/functions/register_taxonomy).

## Setup a WordPress Multisite with 2 connected sites

To setup a WordPress Multisite you can follow our tutorial [How to install and set up a WordPress Multisite.](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/) Our guide [Getting started with MultilingualPress 3](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/#Create-a-new-website-within-the-multisite-and-set-the-language-for-the-site) explains how to create the sites and connect them with MultilingualPress. We created 2 sites, one for English and one for German and connected them as you can see in the screenshot below.

[caption id="attachment_3418" align="aligncenter" width="1353"][![Two connected language Sites in a WordPress Multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/WordPress-multisite-connected-language-sites.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/WordPress-multisite-connected-language-sites.jpg) Two sites in a WordPress multisite for English and German connected with MultilingualPress[/caption]

## Install and setup Custom Post Type UI plugin

In the next step we install and activate the [Custom Post Type UI](https://wordpress.org/plugins/custom-post-type-ui/) plugin. Regarding plugin activation we need to decide if it should be network activated or activated in each site individually. The decision will depend on the plugins ability to support Multisite or not. In this case Custom Post Type UI does not have Multisite support (at least in the free version) so we activate it on each site. To do so, go to the Dashboard of each site and activate the plugin on the _Plugins_ page.

**Please note:** The plugin you use to create the custom post type has to be **network activated in the Multisite environment** or, at least, has to be **activated also in the main network site** in order to make the custom type available across all the network.

[caption id="attachment_3421" align="aligncenter" width="1352"][![Install the plugin Custom Post type UI](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/Install-Custom-Post-Type-UI-plugin.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/Install-Custom-Post-Type-UI-plugin.jpg) Install the plugin Custom Post type UI which we want to use for creating our custom post type and custom taxonomy.[/caption]

## Create a new custom post type and a taxonomy

We first create the custom post type and taxonomy on site 1 and afterwards we will copy them to site 2. We will call our custom post type _Recipes_ and the taxonomy _Ingredients_.

[caption id="attachment_3422" align="aligncenter" width="1355"][![Create a custom post type Recipes](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-custom-post-type.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-custom-post-type.jpg) Create a custom post type Recipes[/caption][caption id="attachment_3423" align="aligncenter" width="1353"][![Create a custom taxonomy Ingredients.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-taxonomy.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-taxonomy.jpg) Create a custom taxonomy Ingredients.[/caption]

To copy the custom post type and taxonomy we use the Export/Import functionality in the _Tools_ page of Custom Post Type UI.

[caption id="attachment_3424" align="aligncenter" width="1354"][![Copy the content of the Export Post Type settings field from site 1...](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/cpt-ui-export-post-type-settings.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/cpt-ui-export-post-type-settings.jpg) Copy the content of the Export Post Type settings field from site 1...[/caption][caption id="attachment_3425" align="aligncenter" width="1355"][![... And paste into the field Import Post Types of  site 2.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/cpt-ui-import-post-types.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/cpt-ui-import-post-types.jpg) ... And paste into the field Import Post Types of  site 2.[/caption]

In the next step we do the same export/import for taxonomies via Taxonomies tab.

## Enable Custom Post Types and Taxonomies in MultilingualPress Settings

Now that we have custom post type and taxonomy created in both sites, we can configure MultilingualPress in order to be able to translate them. To do so go to _My Sites → Network Admin →  Settings →  MultilingualPress_ and enable the custom post type and the taxonomy in the corresponding tabs, in our case _Recipes_ and _Ingredients._

[caption id="attachment_3427" align="aligncenter" width="1356"][![Enable Recipes in Translatable Post Types tab.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-enable-custom-post-type.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-enable-custom-post-type.jpg) Enable Recipes in Translatable Post Types tab.[/caption][caption id="attachment_3428" align="aligncenter" width="1356"][![Enable Ingredients in Translatable Taxonomies tab.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-enable-taxonomy.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-enable-taxonomy.jpg) Enable Ingredients in Translatable Taxonomies tab.[/caption]

## **Translate Post Type slug on each site**

Custom post type slugs can be translated during registration time via the rewrite parameter from [register_post_type](https://codex.wordpress.org/Function_Reference/register_post_type) (e.g., _'rewrite' => ['slug' => esc_html__('my-cpt', 'text-domain-here')]_). When using the CPT UI plugin, the parameter is called **Custom Rewrite Slug**. If you have translated the slugs per site via the rewrite slug, MultilingualPress will automatically detect and use your rewrite slug on the site (e.g., for language switcher or hreflang URLs).

If you did not translate the custom post type slug during registration with a rewrite slug, you can translate it from the Post Type Slugs menu. To do so, navigate to _My Sites → Network Admin → Sites_ and edit each site. In the Post Type Slugs tab, MultilingualPress will automatically display the currently used slug for each custom post type registered on this site. To translate the slug, fill in the translated slug on each site.

**Important**: After changing the Post Type Slug, the permalink settings must be manually saved on the site for the new slugs to be applied.

If your custom post type is greyed out, you may need to enable it in the MultilingualPress settings as a Translatable Post Type.

[caption id="attachment_3483" align="aligncenter" width="1034"][![Enter a slug for your custom post type on each site](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-post-type-slug.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-post-type-slug.jpg) Enter a slug for your custom post type on each site[/caption]

## Create some custom posts and taxonomy terms

We can start creating ingredients (taxonomy terms) and recipes (custom posts) in site 1 and then we use the MultilingualPress translation metabox to create the translations for site 2 from there. It is also possible to connect existing content in site 2 from the same translation metabox.

[caption id="attachment_3484" align="aligncenter" width="1354"][![Create some Ingredients in site 1.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-ingredients-taxonomy-terms.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-ingredients-taxonomy-terms.jpg) Create some Ingredients in site 1.[/caption][caption id="attachment_3485" align="aligncenter" width="1355"][![Create Recipes and assign Ingredients in site 1.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-custom-post-recipes.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/create-custom-post-recipes.jpg) Create Recipes and assign Ingredients in site 1.[/caption]

## Connect Taxonomy Terms with MultilingualPress

After creating the taxonomy terms on the different language sites we need to connect them.  Go to the dashboard of site 1, select _Recipes →_ _Ingredients_ and edit one term. In the translation metabox you can choose _Create a new term_ or _Select an existing term_. In this case we choose _Create a new term_. We can fill the fields in _Term Data_ tab manually otherwise the values will be generated automatically for you.

[caption id="attachment_3486" align="aligncenter" width="1046"][![Connect taxonomy terms in the MultilingualPress translation meta box](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-connect-taxonomy-terms.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-connect-taxonomy-terms.jpg) Connect taxonomy terms in the MultilingualPress translation meta box[/caption]

## Connect Custom Post Types with MultilingualPress

Connecting the custom posts is similar to connecting taxonomy terms. Go to the dasboard of site 1, select _Recipes_ in the menu and edit one.  In the translation metabox you can choose _Create a new Recipe_ or _Select an_ existing _Recipe._ We choose _Create a new Recipe_. You can setup the values manually and use advanced features like _Copy featured image_ in _Advanced_ tab.

[caption id="attachment_3488" align="aligncenter" width="1058"][![Connect custom post types with MultilingualPress](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/Connect-custom-post-type-multilingualpress.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/Connect-custom-post-type-multilingualpress.jpg) Connect custom post types with MultilingualPress[/caption]

Now if you go to site 2 you will see a new _Recipe_ created. Edit it and select a translated taxonomy in the _Ingredients_ metabox:

[caption id="attachment_3489" align="aligncenter" width="1237"][![Select an Ingredients taxonomy term in the taxonomy metabox](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/taxonomy-metaboox.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/taxonomy-metaboox.jpg) Select an Ingredients taxonomy term in the Ingredients taxonomy metabox[/caption]

## Create a menu on each site to navigate through languages

Now that we have some recipes and ingredients connected between both sites we create a menu on each site to allow the user to switch between languages. In the menu we will add MultilingualPress language items.

[caption id="attachment_3492" align="aligncenter" width="1456"][![Create a language menu on each site to allow users to switch languages](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-create-language-menu.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-create-language-menu.jpg) Create a language menu on each site to allow users to switch languages and add language items to it[/caption]

## Setup Permalinks structure

Before we check that switching languages works, we need to ensure that our permalinks structure is configured correctly. Depending on if it is a new Multisite installation it could be that our permalink includes a _/blog/_ slug added by WordPress. The best approach for now is to simply get rid of this part in the permalink:

[caption id="attachment_3493" align="aligncenter" width="1508"][![Remove /blog/ from URLs](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/remove-blog-from-permalink.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/remove-blog-from-permalink.jpg) Remove /blog/ from URLs[/caption]

A quick tip for removing the _/blog/_ slug from the permalink is to select _Plain_ and save. Then select _Custom Structure_ and remove _/blog/_ slug there. You need to remove the _/blog/_ slug in both sites. Don't forget to 301 redirect the old slugs to the new.

## Visit a Custom Post page and switch language

Now that everything is setup correctly, its time to check that we can switch languages from a custom post type page. Go to site 1 and view one of the Recipes you've set up. Then switch languages in the menu. You should be redirected to the translated version. Do the same also for the taxonomy terms.

[caption id="attachment_3497" align="aligncenter" width="1292"][![View a Recipes post](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/view-custom-post.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/view-custom-post.jpg) View a Recipes post ...[/caption]

[caption id="attachment_3500" align="aligncenter" width="1269"][![... and switch the language](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/switch-language-taxonomy-term.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/switch-language-taxonomy-term.jpg) ... and switch the language[/caption][caption id="attachment_3499" align="aligncenter" width="1275"][![View an ingredient...](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/view-taxonomy-term.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/view-taxonomy-term.jpg) View an ingredient...[/caption]

[caption id="attachment_3498" align="aligncenter" width="1148"][![... and switch the language](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-switch-language-custom-post.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/11/multilingualpress-switch-language-custom-post.jpg) ... and switch the language[/caption]

That's all you need to do regarding setting up custom post type and taxonomy translations in MultilingualPress. If you have doubts or need further assistance, just let us know.