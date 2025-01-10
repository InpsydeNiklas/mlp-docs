MultilingualPress version 3.6.0 and higher is now compatible with [Beaver Builder](https://www.wpbeaverbuilder.com/): pages or posts built with Beaver can be managed through the MultilingualPress translation metabox.

Here we provide a brief example to show how this can be achieved.

## **Enable Beaver Builder support in the MultilingualPress settings**

In this tutorial we assume that you have a WordPress Multisite environment properly installed with MultilingualPress and Beaver Builder installed in the network and activated in all subsites.

Besides in our test environment we refer to 3 language sub sites: English, Italian and German. On each site we also set a language menu, in order to easily navigate to the different versions of the content that we are going to create.

For more info about how to set such an environment you can refer to [Getting started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/).

The first step we need to perform is to enable the Beaver Builder module in the MultilingualPress settings.

To do so, we head to _Network Admin Dashboard -> MultilingualPress,_ and in the Module tab we select the _Beaver Builder_ checkbox as reported in the picture below. Click on the _Save Changes_ button to save the settings.

[caption id="attachment_17542" align="aligncenter" width="852"][![Enable Beaver Builder support module](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Module-activation-Beaver-Builder.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Module-activation-Beaver-Builder.png) Enable Beaver Builder support module[/caption]

## Build a page with Beaver Builder

Now that the Beaver Builder module is active in MultilingualPress we go to the English site.

There, we head to _Dashboard-> Pages -> Add New_ . In that way we create a new page and then we proceed setting the title as "_Beaver Builder Test Page_" as shown in the picture below.

[caption id="attachment_17551" align="aligncenter" width="1151"][![Beaver Builder Test Page](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Beaver-Builder-Test-Page.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Beaver-Builder-Test-Page.png) Beaver Builder Test Page[/caption]

Now we save the page as a draft using the related button. Then selecting the "_Launch Beaver Builder_" button we access the Beaver editor. Using Beaver we properly set our page with the page builder tools.

In this case we set a two column section. We add some text in the left column, and embed a YouTube video in the right one. The picture below shows the result.

[caption id="attachment_17553" align="aligncenter" width="920"][![Page edited with Beaver Builder](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Page-edited-with-Beaver-Builder.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Page-edited-with-Beaver-Builder.png) Page edited with Beaver Builder[/caption]

The English content page is ready: we exit the Beaver Builder environment and we go back to the standard WordPress editor. Is time to set the translation with MultilingualPress.

## **Translate the content** with MultilingualPress

In the WordPress editor, we scroll down the page to reach the MultilingualPress translation metabox for the Italian language. Here, in the _Relationship_ tab, we select the radio button option "_Create a new page and use it as a translation in Italian (Italia)_".

Then we head to the tab "_Title and Content_", and we set the _New Post Title_ field as _"Beaver Builder Test Page - Italian"._ In the same tab we also select the checkbox "_Overwrites content on translated post with the content of source post._".

We execute all these actions again in the MultilingualPress translation metabox for the German language. This is available right under the metabox previously set. But this time we set the _New Post Title_ field as _"Beaver Builder Test Page - German"._

[caption id="attachment_17554" align="aligncenter" width="872"][![Translation metaboxes configured](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Translation-metaboxes-Beaver-Builder.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Translation-metaboxes-Beaver-Builder.png) Translation metaboxes configured[/caption]

Finally we save the post with the "_Publish_" button.

The pages are finally set: using the language menu switcher, we can navigate through the different language versions of the page.

This way we can verify the Italian and German version of the content we previously set in the English page is properly set, including all the settings created with Beaver Builder.

[caption id="attachment_17555" align="aligncenter" width="868"][![Beaver Builder Test Page - Italian version](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Beaver-Builder-Test-Page-Italian-version.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Beaver-Builder-Test-Page-Italian-version.png) Beaver Builder Test Page - Italian version[/caption]

[caption id="attachment_17557" align="aligncenter" width="865"][![Beaver Builder Test Page - Italian version](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Beaver-Builder-Test-Page-German-version.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Beaver-Builder-Test-Page-German-version.png) Beaver Builder Test Page - Italian version[/caption]

This is how Beaver Builder works together with MultilingualPress. But there is even more: also Elementor can be easily used together with MultilingualPress. For another example on that topic have a look at [How to translate Elementor content with MultilingualPress](https://multilingualpress.org/docs/how-to-translate-elementor-content-with-multilingualpress/).