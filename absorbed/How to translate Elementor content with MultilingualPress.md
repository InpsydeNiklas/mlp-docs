Starting from MultilingualPress version 3.6.0 is possible to work with [Elementor](https://elementor.com/), one of the leading Website Builders for WordPress! In fact, content built with this website builder can still be managed trough the MultilingualPress translation metabox.

Let's a have a look to an example.

## **Enable Elementor support in MultilingualPress**

The first step is to activate the Elementor module in MultilingualPress.

In our example we refer to a WordPress Multisite environment with MultilingualPress and Elementor installed in the network and activated in all subsites.

Besides, in our test environment we use 3 language subsites: English, Italian and German. On each site we set a language menu, in order to easily navigate to the different versions of the content that we are going to create.

More information about how to set such an environment can be found here: [Getting started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/).

When Elementor is active, we head to _Network Admin Dashboard -> MultilingualPress_ and in the Module tab we select the Elementor checkbox, and click on the _Save Changes_ button.

[caption id="attachment_17475" align="aligncenter" width="859"][![Enabling Elementor support](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Module-activation.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Module-activation.png) Enabling Elementor support[/caption]

With this action we enable Elementor Support for MultilingualPress.

## **Build a page with Elementor**

Now that the Elementor module is active in MultilingualPress, we are going to the English site and build a page with the Pagebuilder.

In the English site, we head to _Dashboard-> Pages -> Add New_ . Now a new page is available and we set the title as “_Elementor Test Page_“.

[caption id="attachment_17478" align="aligncenter" width="953"][![Elementor Test Page](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Elementor-Test-Page.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Elementor-Test-Page.png) Elementor Test Page[/caption]

Next we click on the “_Save as draft_” button to save the page.

After we have clicked the button “_Edit with Elementor_“, it is possible to use Elementor and build our page. In our case we create a section with two columns and include text in the left one, and embed a YouTube video in the right one. This is, what our result looks like:

[caption id="attachment_17505" align="aligncenter" width="830"][![Page edited with Elementor](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Page-edited-with-Elementor.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Page-edited-with-Elementor.png) Page edited with Elementor[/caption]

## **Translate the content with MultilingualPress**

Now we go back to the WordPress editor clicking on the “_EXIT TO DASHBOARD_” button in the Elementor control panel. From here we scroll down to the MultilingualPress translation metabox for the Italian language, where we select the option “_Create a new page and use it as a translation in Italian (Italia)_“.

Then we select the tab “_Title and Content_“, and there we proceed filling in the title for the remote post as _“Elementor Test Page – Italian”,_ and also selecting the checkbox “_Overwrites content on translated post with the content of source post._“.

Finally, we perform the same actions again with the MultilingualPress translation metabox for the German language, this time setting the title for the remote post as _“Elementor Test Page – German” ._

[caption id="attachment_17507" align="aligncenter" width="757"][![Translation metaboxes configured](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Translation-metaboxes.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Translation-metaboxes.png) Translation metaboxes configured[/caption]

Now we can save the post clicking on the “_Publish_” button.

Using the main menu it is possible to navigate through the different language versions of the page. As we can see, the content provided for the English version of our page has been duplicated in the Italian and German version, including the settings created with the Elementor website builder.

[caption id="attachment_17508" align="aligncenter" width="830"][![Elementor Test Page - Italian version](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Elementor-Test-Page-Italian-version.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Elementor-Test-Page-Italian-version.png) Elementor Test Page - Italian version[/caption]

[caption id="attachment_17509" align="aligncenter" width="812"][![Elementor Test Page - German version](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Elementor-Test-Page-German-version.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/05/Elementor-Test-Page-German-version.png) Elementor Test Page - German version[/caption]

By the way, Elementor is not the only website builder compatible with MultilingualPress: Beaver Builder can also be used with our plugin.

More information can be found here: [How to translate Beaver Builder content with MultilingualPress](https://multilingualpress.org/docs/how-to-translate-beaver-builder-content-with-multilingualpress/).