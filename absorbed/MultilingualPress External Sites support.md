Starting from version 4.3.0 of MultilingualPress, you can activate a module that links source posts from a subsite of the network that has MultilingualPress installed with a page on an external site.

## Setting up an External Site

First, proceed to the Network dashboard and access the MultilingualPress admin panel to activate the module ([MultilingualPress Global Settings](https://multilingualpress.org/docs/getting-started-with-multilingualpress/#Global-settings-for-MultilingualPress)). As shown in the figure, select the _External Sites_ checkbox on this panel and press the _Save Changes_ button to activate the module.

[caption id="attachment_26498" align="aligncenter" width="1468"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/1_activate_module_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/1_activate_module_en.png) Activate the External Sites module[/caption]

Now, selecting the External Sites link on the left menu can access the External Sites section and create an external site link. In this case, we will create a link to an Italian newspaper site page.

[caption id="attachment_26512" align="aligncenter" width="1897"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/1.2_create_external_site_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/1.2_create_external_site_en.png) Create an External Site.[/caption]

If you wish to redirect the user to the external site automatically, the Redirection module must also be activated in the MultilingualPress settings.

[caption id="attachment_26500" align="aligncenter" width="1279"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/3_activate_redirection_module_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/3_activate_redirection_module_en.png) Activate Redirection module in MultilingualPress Settings[/caption]

Only in this case, the option for automatic redirection is visible in the External Site creation form, as depicted in the figure below.

[caption id="attachment_26499" align="aligncenter" width="1705"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/2_activate_redirection_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/2_activate_redirection_en.png) Activate redirection[/caption]

Remember to select the “Enable Automatic Redirect” checkbox to allow automatic redirection to the External Site for all those users whose language matches the one set for the respective external site.

So, an External Site is defined by the following parameters:

- **Site URL** _(required)_: Defines the URL of the external site where you intend to redirect the user.
- **Site Language Name** _(required)_:  The name you wish to give to the external link, either to edit it in the backend or to appropriately name the translation in the language menu.
- **Site Language Locale** _(required)_: The locale for the language to which the external site is associated.
- **Enable Hreflang**: Using the hreflang attribute for language and regional targeting.
- **Enable Automatic Redirect**: The option to enable automatic redirection of the user; is visible only if the Redirect module has been activated in the MultilingualPress settings.

Finally, suppose the Enable Automatic Redirect option is activated in the MultilingualPress settings. In that case, a new select box is added to display the list of defined External Sites in the Redirection tab. You can select an External Site from this list to designate it as the fallback external redirection link, as shown in the picture below.

[caption id="attachment_26502" align="aligncenter" width="1383"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/4_select_external_redirection_fallback_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/4_select_external_redirection_fallback_en.png) Redirection: External fallback site[/caption]

## Referencing a post to an External Site

Suppose we have a page or a post created in one sub-site. If we head into the post in edit mode, we can see a new section with the MultilingualPress translation meta boxes where the defined External Sites are shown.

[caption id="attachment_26504" align="aligncenter" width="1507"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/5_post_backend_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/5_post_backend_en.png) External sites translation metabox[/caption]

If no URL is specified in the field related to the External Site, the translation link will redirect the user to the URL defined in the MultilingualPress settings. If we want to define a specific URL, this can be done by filling in the field next to the related External Site name.

## **Adding an External Site to the language menu**

After setting up the External Site redirection feature and properly assigning the link to a post, we need to add a new element in the language menu that lets us manually switch to the translation managed by the External Site.

Our original post, “India on the Moon,” is linked to an article on an external Italian site: We need to provide the language menu with an item that lets the user manually switch to that site. To do so, we update the menu as reported in the following image.

[caption id="attachment_26506" align="aligncenter" width="1871"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/6_update_menu_en.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/6_update_menu_en.png) Add External site to the language menu[/caption]

Pressing the _Save Menu_ button, the menu is updated. The language menu lets users select the Italian External Site directly from the frontend.

[caption id="attachment_26507" align="aligncenter" width="1015"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/7_frontend.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/08/7_frontend.png) Menu with the External Site switch link[/caption]