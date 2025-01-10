Would you like to create a multilingual website quickly and easily? MultilingualPress (MLP) is the perfect choice.

## What exactly can MultilingualPress do?

MultilingualPress establishes **language connections** between various pages on a WordPress multisite. This enables you to display content to your website visitors in their language. To do so, you set up each different language version of your website as a site within a WordPress multisite. Then, you link the translated content using MultilingualPress. Content can include posts, pages, custom post types or even so-called taxonomies. This last designation includes categories and keywords, for example.

Our plugin also helps you  forward website visitors to their appropriate language versionand automatically assists you with search engine optimization for your multilingual website.  

## Check out our MultilingualPress video

Do you prefer watching a video instead of reading a long text? Do you want to know what MultilingualPress looks like in the backend and see how  easy it is to  use before buying? Take a look at our product video [here](https://www.youtube.com/watch?v=aO4AYVl2eOQ).

If the video did not answer all your questions, please continue reading on this page or contact us.

## What are the requirements for using MultilingualPress?

To install MultilingualPress, you need:

- _An installed version of WordPress Multisite with WordPress >= 4.8_
- _PHP version >=7.4_

If you don’t have WordPress Multisite yet, please follow our guide [Installing and setting up WordPress Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/). You can find more tutorials for _WordPress Multisite_ in our guide [WordPress Multisite 1x1](https://multilingualpress.org/docs-category/wordpress-multisite-1x1/).

## Installing MultilingualPress

**Please note:** Do not use MLP 2 and MLP (3 and higher) together in one multisite. For updating from version 2 to version 3+, try our [MultilingualPress Migration Tool](https://multilingualpress.org/docs/multilingualpress-2-3-migration-tool/).

1. After you have [purchased MultilingualPress](https://multilingualpress.org/#buy), please log in to your [customer account](https://multilingualpress.org/my-account/) and download the product.
2. Go to _My Sites → Network Admin → Plugins_, upload the plugin, and activate it across the network.
3. Then go to _My Sites → Network Admin → MultilingualPress_ and enter your Master API Key and Product ID in the _License_ tab. These can be found in your [customer account](https://multilingualpress.org/my-account/).[caption id="attachment_13873" align="aligncenter" width="1103"][![MultilingualPress license data and product download in your customer account](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-License-download-customer-account.png.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-License-download-customer-account.png.png) MultilingualPress license data and product download in your customer account[/caption][caption id="attachment_13875" align="aligncenter" width="1831"][![Activate MultilingualPress license](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-license-activate.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-license-activate.png) Activate your MultilingualPress license[/caption]

## Global settings for MultilingualPress

To change global settings, go to My Sites → Network Admin, then click on the left menu on MultilingualPress. In addition to the License tab, you will find here six tabs with settings that apply for all sites. Two of these tabs will be available only when the related modules Redirect and Quicklinks are activated.

[caption id="attachment_26105" align="aligncenter" width="627"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/GlobalSettings-1.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/GlobalSettings-1.png) MultilingualPress Modules Settings[/caption]

- **Modules** – On this tab, you can activate or completely deactivate MultilingualPress features:
    - _Gutenberg Blocks:_activates the support for the MultlingualPress blocks.
    - _Alternative language title:_ activates the feature “Alternative language title”. If you check this box, a field for the alternative language title will appear on the MultilingualPress settings page for the website in question. This will be displayed in the Admin menu instead of the website title that was set when the site was created.
    - _Redirect_: activates the feature for automatic language redirection. When this module is enabled a new tab “Redirection” will be activated. Further information is available below, on the Redirection tab description.  
        When this module is enabled, on the MultilingualPress settings page of the subsite (available when a new subsite is created or edited), two fields are available: the first to activate the automatic language redirection, the second one to specify if the current subsite has to be used as a fallback for the root language set.  
        That means, for example in the case of Italian root language used in two subsites, that: if site A has Italiano(Italia) language and site B has Italiano(San Marino) language and site A has the Redirect Fallback site for this language option checked, any customer who tries to access an Italian version which is not Italia or San Marino kind, is automatically redirected to the subsite A.  
        Further information is also available at: [MultilingualPress release 3.9.0](https://multilingualpress.org/multilingualpress-release-3-9-0/).[caption id="attachment_20991" align="aligncenter" width="1077"][![Settings for each site – Checkbox for alternative language title and checkbox for automatic redirect](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Redirection-Settings-EN.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Redirection-Settings-EN.png) Settings for each site – Checkbox for alternative language title and checkbox for automatic redirect[/caption]
    - _Trasher_: if this checkbox is activated, when editing a post, in the “Publish”meta box a checkbox will be displayed saying “Send all the translations to trash when this post is trashed.” Check this box to delete all translations of the post simultaneously if you move one of them to the trash.[caption id="attachment_2079" align="aligncenter" width="1200"][![Activate MultilingualPress Trasher checkbox to move all translations of a specific post into the trash simultaneously.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-trasher-checkbox.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-trasher-checkbox.png) Activate the MultilingualPress Trasher checkbox to move all translations of a specific post into the trash simultaneously.[/caption]
    - _Language Manager:_ This enables the Language Manager, which allows you to include custom languages or override existing ones. You can find the Language Manager under _My Sites → Network Admin → MultilingualPress → Language Manager_. Click the New Language button to add a new line for a language to be added and enter your preferred settings in the fields. You can also search for an existing language and adapt it.
    - _Language Switcher:_ This enables the Language Switcher Widget which allows you to quickly include a language switcher in the locations set through your theme.
    - _WooCommerce_: This module enables WooCommerce support and allows you to translate WooCommerce products, orders and coupons but also the product attributes typical to WooCommerce (product categories and product tags).
    - _Quicklink_: This module enables the rendering of a link in the front end for each post translation; a dedicated tab section is available to set the position of the links.
    - _ACF_: This module can be enabled when the plugin [Advanced Custom Fields](https://wordpress.org/plugins/advanced-custom-fields/) is also installed and activated in the Network. Through this module MultilingualPress will be able to manage these fields correctly. More information are available [here](https://multilingualpress.org/docs/how-to-translate-advanced-custom-fields-acf-with-multilingualpress-3/)
    - _Beaver Builder_: This module enables the compatibility mode between MultilingualPress and Beaver Builder, in order to enable compatibility with this Page Builder plugin. Further information is available [here](https://multilingualpress.org/multilingualpress-release-3-6-0/).
    - _Elementor_: This module enables the compatibility mode between MultilingualPress and Elementor, in order to enable compatibility with this Page Builder plugin. Further information is available [here](https://multilingualpress.org/multilingualpress-release-3-6-0/)
    - _User Information Translation Settings_: This module enables the translation for the field “Biographical Info” available in the user profile section in the WordPress backend; when active, is possible to add a separated translation for the “Biographical Info” for each language site available in the Multisite.  
        
    - _Original Translation Language_: This module enables a checkbox that can be used, when editing a post, to specify if the content is the original one or instead is just a translation of another post.
    - _Comments_: This module enables the support for comments, more information is available here: [MultilingualPress Comments support](https://multilingualpress.org/docs/multilingualpress-comments-support/).
    - _External Sites_: This module enables the support for external sites, more information is available here: [MultilingualPress External Sites support](https://multilingualpress.org/docs/multilingualpress-external-sites-support/).
    - _MultilingualPress Site Flags_: This module lets you automatically add the language flags into your menu. When activated, it also renders, when a new site is created, a flag-style menu (Menu Language Style) to select and a field (Custom Site flag) used to add an image URL in order to display it as a custom flag for the current site.  
        [caption id="attachment_20632" align="aligncenter" width="1271"][![Style the flags menu](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MLP-Menu-Flag-Style-EN.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MLP-Menu-Flag-Style-EN.png) Style the flags menu[/caption]
    - _WooCommerce Brands_: This module enables the compatibility mode between MultilingualPress and the Woocommerce Brands plugin, in order to avoid a taxonomy slug conflict. Further information is available [here](https://multilingualpress.org/multilingualpress-release-3-5-0/)
- **Translatable Post Types:** All content types (post types) are displayed here for which MultilingualPress can create a language relation. Select the type of your choice. The corresponding meta boxes will only be available for this post type during editing. For instance, if you only select Posts, then you will only be able to link content in different languages for posts.[caption id="attachment_17148" align="aligncenter" width="1514"][![Set translatable content types with MultilingualPress](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/TranslatableContent-Types.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/TranslatableContent-Types.png) Set translatable content types with MultilingualPress[/caption]
- **Translatable Taxonomies:** Like Translatable Post Types, but for taxonomies. Taxonomies include for example categories or tags.[![](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/TranslatableContent-Taxonomies.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/TranslatableContent-Taxonomies.png)
- **Redirect**: This tab is enabled only when the related option module is checked in the Modules tab.  
    Here, you find three select boxes:
    - _Redirect Fallback_: is a network site where the user is directed in case his/her language is not available in any of the sites set in the network
    - _Redirect Execution_: this is the programming (PHP or JavaScript) language that will be used for the redirection 
    - _Redirect Type_: this lets you choose how the redirection should work. We have three options:
        - - _Browser language (Header):_ the redirection is performed by detecting the browser language and redirecting the user to the related country site if it exists,  to the fallback site if it exists, or no action will be performed    
            - _Geolocation (IP Address):_ the redirection is performed by detecting the IP address of the visitor and using the [geoplugin](https://www.geoplugin.com/) service will detect the country and will redirect to that country site if it exists, otherwise to the fallback site, or no action will be performed   
            - **_Geolocation with fallback to browser Language:_ the redirection is performed by detecting the IP address of the visitor and then using the [geoplugin](https://www.geoplugin.com/) service will detect the country and will redirect to that country site if it exists; otherwise, it will default to the first option (Browser language)**[![MultilingualPress Redirect Fallback](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Redirect.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Redirect.png)
- **QuickLinks**: This tab is enabled only when the related option module is checked in the Modules tab.  
    The four radio buttons here let you select the position of your quicklinks related to the content of the post. The links to the translation will be available only if some content exists in the related translation post linked.[caption id="attachment_13880" align="aligncenter" width="1355"][![MultilingualPress QuickLinks](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-QuickLinks-1.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-QuickLinks-1.png) MultilingualPress QuickLinks[/caption]
- **Cache:** This option lets you enable or disable selectively the MultilingualPress cache components. Cache helps in improving the plugin performance. But in case there are conflicts with the server cache and/or with other plugins, it is possible to select and disable all, or only some, of the components.[caption id="attachment_13881" align="aligncenter" width="1368"][![MultilingualPress cache options](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Set-Cache-options-with-MultilingualPress.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Set-Cache-options-with-MultilingualPress.png) MultilingualPress cache options[/caption]

## Create a new website within the multisite and set the language for the site

1. Go to _My Sites_ _→_ _Network Admin_ _→_ _Sites_ and click on the button _Add New_.[caption id="attachment_2072" align="aligncenter" width="1200"][![Add a new website to the network](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-network-sites.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-network-sites.png) Add a new website to the network[/caption]
2. On the settings page that appears, enter the following information in the upper section:
    
    - _Site Address (URL)_- the URL of your new website
    - _Site Title_ – This will be displayed in the Admin menu and potentially on the frontend as well
    - _Site Language_ – In this case, this is the backend language for the site, the language for translation will appear further down
    - _Admin Email -_ the email of the site admin
    
    These are all settings of the WordPress multisite that are available without MultilingualPress.
    
    [caption id="attachment_2314" align="aligncenter" width="1021"][![Add a new website to the network: the general settings of WordPress multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/add-new-site-to-wordpress-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/add-new-site-to-wordpress-multisite.png) Add a new website to the network: the general settings of WordPress multisite[/caption]
3. There is an area with information for MultilingualPress. You can change most of these settings later by going to My Sites → Network Admin → Sites, editing the site of your choice,and accessing the tab _MultilingualPress_:
    
    - _Language_ – This is the language selection. For instance, if the content on this website is supposed to be in French, then choose French here. MultilingualPress offers you many more languages to choose from than WordPress. This language field is not the standard WordPress locale language, for further information have a look at _Do not override WordPress locale and let WordPress default setting to manage the site language_ at [MultilingualPress release 3.9.0](https://multilingualpress.org/multilingualpress-release-3-9-0/).
    - _Relationships_ – The websites you would like to link with this site. For every language which you would like to translate on your site, you should create a website and link them all together.
    - _Based on site_ – If you select a website here, a copy of this website will be generated when you create the new website, saving you lots of work in configuring and creating content.
    - _Copy Attachments_ – If the option is checked all the attachments of the source site will be copied in the destination site. Sometimes, due to hosting restrictions, this process cannot be performed or takes too much time to be properly accomplished. In that case if you do not check the option the attachments will not be automatically copied: instead this could be manually done after the duplication process is executed.
    - _Connect content_ – If this option is checked the new site will have all the content connected with the source site; by default the checkbox is checked so all content will be connected.
    - _Connect comments_ – If the option is checked, the new site will have all the comments connected with the source site; for further information check [MultilingualPress Comments support](https://multilingualpress.org/docs/multilingualpress-comments-support/).
    - _Plugins_ – Check the box here to activate all plugins on the new website that are active on the source website.
    - _User__s –_Check the box here to copy all the users on the source website to the new website.
    - _Search Engine Visibility_ – As usual for WordPress, you can check the box here to prevent search engines from indexing the site.
    - _Alternative Language Title_ – here you can set a title for your website that will be displayed in the Admin menu instead of the title indicated above. This field will only be displayed if you activate the module _Alternative language title_ in the global settings of MultilingualPress.
    - _Redirect –_Check these boxes to activate the automatic language forwarding. These fields will only be displayed if you activate the module Redirect in the global settings of MultilingualPress. Select the option you need, in order to enable the redirection for this site and/or to select this site as a root language fallback site (see the previous section for further information).
    
    [caption id="attachment_26101" align="aligncenter" width="1192"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/settings-add-a-new-site.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/settings-add-a-new-site.png) Settings - Add a new site[/caption]

## Translate and link content with MultilingualPress

After lots of preparation, we have arrived  at the most important feature of MultilingualPress: translating posts and linking translations together. We make a distinction between translating content types (posts, pages, sites, products etc.) and translating taxonomies (categories, tags etc.).

### Translating sites and posts

Please edit this in one of the sites to translate a post.. Enter your heading, URL and text as normal for this site. Below the editor you will find the MultilingualPress meta boxes to translate the post into other languages, one meta box per language. The meta box includes the following tabs: _Relationship_, _Title_ and _Content_, _Excerpt_, _Advanced_ and _Taxonomies._ We will briefly explain all tabs here. Enter your settings for the language connection or translation in the tabs and then save the post.

- **Relationship:** Here you can specify a language connection, that is, selecting which post is the translation of the post you are currently editing. You have the option of not choosing any translation, creating a new post or setting an existing post as the translation. If a link already exists, you can also remove it.[caption id="attachment_2077" align="aligncenter" width="1200"][![Translating a post with MultilingualPress: set language connection, i.e. link translations together.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-metabox.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-metabox.png) Translating a post with MultilingualPress: set language connection, i.e. link translations together.[/caption]
- **Title and c****ontent: Here you can enter the title and content of the linked post. If you check the box next to _Copy source content_, this will overwrite the current content of the translation with the content in the post you are translating.**[caption id="attachment_2352" align="aligncenter" width="1258"][![Translating a post with MultilingualPress: Enter the title and content of the translation](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-title-content.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-title-content.png) Translating a post with MultilingualPress: Enter the title and content of the translation[/caption]
- **Excerpt:** In case you want to enter an excerpt for the translation, you can do so here.[caption id="attachment_2357" align="aligncenter" width="1257"][![Translating a post with MultilingualPress: Enter an excerpt for the translation](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-excerpt.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-excerpt.png) Translating a post with MultilingualPress: Enter an excerpt for the translation[/caption]
- **Advanced:** In this tab you can specify the URL (Post Slug) and status (published, draft, pending) of the translation. You also have the option of copying the picture from the original post into the translation. At the bottom, you will find a link that will take you to Edit mode for the translation. Clicking the link opens the linked post for editing. To translate the actual content please switch to the connected post using this link in the editor.[caption id="attachment_2362" align="aligncenter" width="1252"][![Translating a post with MultilingualPress: The Advanced tab with Slug, Post status, Post image and Link to editor for translation](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-advanced.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-advanced.png) Translating a post with MultilingualPress: The Advanced tab with Slug, Post status, Post image and Link to editor for translation[/caption]
- **Taxonomies**: Here you can specify taxonomies (e.g. categories, tags) for the translation. _Synchronize taxonomies_ overwrites all existing taxonomies in the translation with those from the source post.[caption id="attachment_2365" align="aligncenter" width="1256"][![Translating a post with MultilingualPress: Specifying taxonomies](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-taxonomies.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-post-taxonomies.png) Translating a post with MultilingualPress: Specifying taxonomies[/caption]

### Translating taxonomies

Taxonomies categorize or group together content in WordPress. The standard taxonomies are categories and tags. There are also so-called custom taxonomies that are supplied by plugins, for instance WooCommerce product features. The different groupings in a taxonomy are called terms. For instance, if you use the tags _News_ and _Tips_ for your posts, then _News_ and _Tips_ are terms within the taxonomy of tags. You can translate taxonomies just like you translate posts.

Enter the left backend navigation for the taxonomy of your choice to do so. Then, select the term you would like to translate. Enter the settings for the translation in the MultilingualPress meta boxes below the editor. The translation meta boxes have only two tabs, in contrast to the posts:

- **Relationship: Here you can specify the language connection. This means you are connecting the terms of the individual languages together. You have the option of not choosing any translations, creating a new term or setting an existing term as the translation. If a link already exists, you can also remove it. If you create a new tag, visit the Term Data tab to define the term attributes before saving.**[caption id="attachment_2430" align="aligncenter" width="1138"][![Translating WordPress taxonomies with MultilingualPress: Specifying language connection](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-taxonomy-connection.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-taxonomy-connection.png) Translating WordPress taxonomies with MultilingualPress: Specifying language connection[/caption]
- **Term data:** Here you can enter the term name, term slug and a description.[caption id="attachment_2431" align="aligncenter" width="1130"][![Translating WordPress taxonomies with MultilingualPress: Specifying term data](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-taxonomiy-term-data.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-translate-taxonomiy-term-data.png) Translating WordPress taxonomies with MultilingualPress: Specifying term data[/caption]

### Translating WooCommerce products

Many of our customers operate multilingual shops with WooCommerce. Therefore, we would like to briefly address the topic of translating WooCommerce products. Generally, this works exactly the same as for other content types and taxonomies described above.

Important: In the global settings of MultilingualPress, choose all WooCommerce content types and taxonomies that you want to be translatable. For WooCommerce this could mean products, coupons, orders, product tags and/or product categories.

If you have set products to be translatable, then you will find the MultilingualPress meta boxes below the product editor. As usual, you can link products together, translate titles, URLs, excerpts and change any other settings as you like.

[caption id="attachment_4030" align="aligncenter" width="1264"][![Translating WooCommerce products and linking the translations together.](https://multilingualpress.org/wp-content/uploads/sites/12/2018/12/Woocommerce-MultilingualPress-Product-Translation.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/12/Woocommerce-MultilingualPress-Product-Translation.png) Translating WooCommerce products and linking the translations together.[/caption]

#### Product data tab

Compared with the previous meta boxes of translation, a new tab specification is available: “Product Data”. Through this tab is possible to set several fields and/or options to properly create or update the related remote site product. Depending on the type of product selected, Product Data tab fields update accordingly with the data available for that type of product.

Some options are specific to a particular product type, while others are present in several or all product types. First of all let’s consider the specific ones. So here is a list of the product types:

- Simple Product
- Grouped Product
- External/Affiliate Product
- Variable Product

Here follows a brief description of the specific options related to each product type that is possible to set.

#### Simple Product

For the Simple Product, the **Regular Price** and **Sale Price** fields are available in the metabox to save and copy prices to the related language site product.

[caption id="attachment_4034" align="aligncenter" width="1272"][![WooCommerce MultilingualPress Product Data – Simple Product, Price Settings](https://multilingualpress.org/wp-content/uploads/sites/12/2018/12/WooCommerce-MultilingualPress-ProductData-SimpleProduct-Price.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/12/WooCommerce-MultilingualPress-ProductData-SimpleProduct-Price.png) WooCommerce MultilingualPress Product Data – Simple Product, Price Settings[/caption]

As we see in the following pictures, files and settings in the **Downloadable** area in the WooCommerce product, can also be copied to the related language site product through the proper checkbox in the translation metabox.

[caption id="attachment_18818" align="aligncenter" width="1279"][![WooCommerce MultilingualPress – Simple Product, Downloadable options](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/WooCommerce-MultilingualPress-Downloadable-option-EN.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/WooCommerce-MultilingualPress-Downloadable-option-EN.png) WooCommerce MultilingualPress – Simple Product, Downloadable options[/caption][caption id="attachment_18819" align="aligncenter" width="1493"][![WooCommerce MultilingualPress Product Data – Downloadable Product](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/WooCommerce-MultilingualPress-Product-Data-–-Downloadable-Product-EN.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/WooCommerce-MultilingualPress-Product-Data-–-Downloadable-Product-EN.png) WooCommerce MultilingualPress Product Data – Downloadable Product[/caption]

In a similar way **Upsells** and **Cross sells** products can be copied to the related product in the remote language site.

Pay attention: in order to properly use this option, the selected Upsells and Cross sells products should exist and be connected in the related destination site beforehand.

[caption id="attachment_18820" align="aligncenter" width="1499"][![WooCommerce MultilingualPress Product Data – Simple Products, Linked Products](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/WooCommerce-MultilingualPress-Product-Data-–-Simple-Products-Linked-Products-EN.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/WooCommerce-MultilingualPress-Product-Data-–-Simple-Products-Linked-Products-EN.png) WooCommerce MultilingualPress Product Data – Simple Products, Linked Products[/caption]

#### Grouped Product

When we use a Grouped Product, checkboxes of the **Grouped** and **Upsells** products in the translation metabox can be set to copy them to the related destination site product. Like the Upsell and Cross sell product in the previous paragraph, it is important to remember that the products should exist and be connected to the related destination site beforehand.

#### External/Affiliate Product

In case we use the External/Affiliate product type, in the product General panel, the fields **Product URL** and **Button Text** are available to copy the related values to the remote language site product.

[caption id="attachment_4039" align="aligncenter" width="1272"][![WooCommerce MultilingualPress Product Data – External Product](https://multilingualpress.org/wp-content/uploads/sites/12/2018/12/WooCommerce-MultilingualPress-ProductData-ProductType.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/12/WooCommerce-MultilingualPress-ProductData-ProductType.png) WooCommerce MultilingualPress Product Data – External Product[/caption]

#### Variable Product

Finally, in case we deal with Variable Product, it is possible to copy all related data by selecting the **Attribute** and **Variations** checkboxes.

After examination of the specific options related to each product type, we are now going to take a look at the common Options shared across several product types.

#### Common Options

Here below the list of common options:

- **Product Type**: by selecting the Product Type checkbox it is possible to change the related remote language site product type
- **SKU**: use this field in the Inventory area to copy SKU to the related language site product
- **Manage stock?**: use this field in the Inventory area to enable stock management at product level
- **Stock quantity**: (only available if field “Manage stock?” is checked) use this field in the Inventory area to set the stock quantity for the product
- **Allow backorders?**: (only available if the field “Manage stock?” is checked) use this field in the Inventory area to control whether or not backorders are allowed. If enabled, stock quantity can go below 0.
- **Low stock threshold**: (only available if the field “Manage stock?” is checked) use this field in the Inventory area to set a product stock value that, when reached, will be notified by email.
- **Sold individually**: use this field in the Inventory area to only allow one of this product to be bought in a single order
- **Gallery**: copies the gallery images to the related language site product
- **Product Short Description**: lets you copy the product description to the related language site product
- **Purchase Note**: lets you copy the Purchase note to the related language site product
- **Inventory Settings**: by selecting this checkbox it is possible to override all the Inventory Settings in the related remote product with the values set in the source product

To specify additional product characteristics for other languages that are not addressed in the previous paragraphs, edit the product in the corresponding site within your multisite.

Please note: WooCommerce shops for individual versions in different languages are independent of one another and have separate shopping carts, inventory etc. MultilingualPress merely links the content together. But if you need a solution for a single stock shared by all shops in the multisite, we have another plugin that accomplishes that task: [Central Stock for WooCommerce](https://wp-centralstock.com/).

## Forward website visitors to the right language version

How will visitors to your website access the version of your multilingual website in a language they speak and understand? There are two options for this: either automatic language redirection or selecting the language from a menu.

### Automatic language redirection

Visitors to a multilingual website are forwarded to the preferred language version of the site based on the language settings in their browser with automatic language redirection. Carry out the following steps to set up this feature in MultilingualPress:

1. Activating the _Redirect_ module_: My Sites_ _→_ _Network Admin_ _→_ _MultilingualPress_ _→_ _Modules._ (see section G_lobal settings for MultilingualPress_)
2. Go to _My Sites_ _→_ _Network Admin_ _→_ _Sites._Edit the sites that contain your website in one language and set a language in the tab _MultilingualPress_.
3. When you have assigned a language to every site, link them together. To do so, go to _My Sites_ _→_ _Network Admin_ _→_ _Sites._  Edit the sites and specify the connections in the tab _MultilingualPress_.
4. You must also link the individual content of the sites together. You can do this in the MultilingualPress meta boxes below the editor. (see section _Translate and link content with MultilingualPress_)

You already completed steps 2 to 4 when translating the content.

[caption id="attachment_2437" align="aligncenter" width="748"][![Browser language settings using Google Chrome as an example (found in Chrome under Settings → Languages)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/browser-language-settings.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/browser-language-settings.png) Browser language settings using Google Chrome as an example (found in Chrome under Settings → Languages)[/caption]

### Selecting the language from a menu

The latest version of MultilingualPress allows you to easily use a Gutengerg Menu Block to set up a language switcher menu. For more details, consult the document following this link: [MultilingualPress Block Menu](https://multilingualpress.org/docs/how-to-set-and-use-the-multilingualpress-block-menu/).

If, on the other hand, you want to create a menu manually, proceed as follows.

In this case, you create a menu for each site within your multisite that contains links to the different language versions of your content. Then, assign a location for the menu as usual in WordPress.

If you link translations together when translating a post, a site etc., then your visitors can switch between the different translations of the post, site etc. using this menu.

Besides, the menu creation on every subsite can be quickly accomplished using the _copy navigation menu_ feature available in MultilingualPress. Further details can be found [here](https://multilingualpress.org/docs/how-to-copy-the-navigation-menu/).

[caption id="attachment_2439" align="aligncenter" width="1349"][![Creating the navigation menu for languages](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/mltilingualpress-create-language-menu.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/mltilingualpress-create-language-menu.png) Creating the navigation menu for languages[/caption]

Note: If the Languages are not available when creating the menu, please click on _Screen Options_ in the top right and check the _Languages_ option.

If instead, you don’t want to create a menu, you can use the MultilingualPress Language Switcher widget: this will quickly set up a language switcher in the position available in your theme. Remember to first activate the related module in the MultilingualPress Settings Module tab to access that widget.

[caption id="attachment_7920" align="aligncenter" width="1544"][![MultilingualPress Language Switcher Widget](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-Language-Switcher-Widget-1.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/MultilingualPress-Language-Switcher-Widget-1.png) MultilingualPress Language Switcher Widget[/caption]

You can also use the widget Navigation menu to display your menu in the sidebar.

[caption id="attachment_2440" align="aligncenter" width="1401"][![Integrating the MultilingualPress language menu using a widget](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-language-widget.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-language-widget.png) Integrating the MultilingualPress language menu using a widget[/caption][caption id="attachment_2443" align="aligncenter" width="1121"][![MultilingualPress language menu in the front end: integrated top right as a menu, in the sidebar as a widget](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-language-menu-frontend.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-language-menu-frontend.png) MultilingualPress language menu in the front end: integrated top right as a menu[/caption]

Finally, consider that each element of the language menu can be rendered with the related country flag: to achieve that, just activate the MultilingualPress Site Flag module on the global settings.

## Displaying hreflang and its significance for SEO

If you are operating a website professionally, it is also important for you to pay attention to [search engine optimization](https://en.wikipedia.org/wiki/Search_engine_optimization) (SEO).

For multilingual websites, you are sure to encounter the term _hreflang_ in connection with SEO. _hreflang_ is a link attribute (rel=”alternate” hreflang=”x”) that is displayed in the heading of a site. It signals to the search engine that the website is multilingual. This also indicates the language the currently displayed content is written and in which other languages it is available, as well as precisely where.

If you implement _hreflang_ incorrectly on your multilingual website, this could cause major problems. This includes the dreaded [duplicate content,](https://www.sistrix.com/ask-sistrix/onpage-optimisation/duplicate-content/) or search engines showing the wrong language version in search results.

MultilingualPress automatically displays _hreflang_ correctly for you once you have linked the translations together. See section _Translate and link content with MultilingualPress._ You can find detailed information about hreflang in the document: [What is hreflang and how to use it in MultilingualPress](https://multilingualpress.org/docs/hreflang-seo-multilingual-wordpress-websites/).

[caption id="attachment_2445" align="aligncenter" width="1326"][![Displaying hreflang in code using MultilingualPress on our demo site demo.multilingualpress.org](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Mulltilingualpress-hreflang-site-code.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Mulltilingualpress-hreflang-site-code.png) Displaying hreflang in code using MultilingualPress[/caption]

## What is the difference between MultilingualPress 3+ and MultilingualPress 2?

From  MultilingualPress version 3 onwards, we have released a completely refactored product with state-of-the-art code and [PHP 7 as recommended by WordPress](https://inpsyde.com/en/wordpress-recommended-php-version-update-php/). We have significantly improved the user interface and ensured compatibility with the [WordPress Gutenberg Editor](https://inpsyde.com/en/wordpress-5-0-gutenberg-editor/). We are also planning new features that we won't include in version 2. Read more in the following post: [https://multilingualpress.org/docs/whats-new-multilingualpress/](https://multilingualpress.org/docs/whats-new-multilingualpress-3/)

## Can I upgrade from MultilingualPress 2 to MultilingualPress 3+?

Upgrading from MultilingualPress 2 to MultilingualPress version 3 and higher is currently possible using a migration module that we recently implemented. You are using MLP 2 and would like to switch to the new version? Check out our migration tutorial: [MultilingualPress Migration Tool](https://multilingualpress.org/docs/multilingualpress-2-3-migration-tool/)

Note: If you purchase MultilingualPress, you also buy ongoing support for Version 2.