Starting from version 3.5 MultilingualPress offers a new module that lets you easily manage the custom fields translation through the Plugin _Advanced Custom Fields (ACF)_. To show how this feature works in your Multilingual site, here we provide a brief tutorial on the topic.

**Note:** For custom fields created by using other Plugins or the [WordPress API for custom fields](https://wordpress.org/support/article/custom-fields/), we recommend [this tutorial](https://multilingualpress.org/docs/how-to-translate-custom-fields-with-multilingualpress-3/).

## Environment settings: WordPress Multisite and MultilingualPress

First of all, create a Multisite WordPress installation and then install MultilingualPress version 3.5 or above. In case you need support to install a multisite environment, you can follow the instruction here reported: [how-to-install-wordpress-multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/)

When your Network is ready you can then proceed in installing and network activating MultilingualPress. Also in this case, if you need support you can refer to the following document: [Installing-MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/#Installing-MultilingualPress-3)

You are just a step far for creating your Multilingual site: proceed in creating two or more subsites as explained in [Create-a-new-website-within-the-multisite-and-set-the-language-for-the-site](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/#Create-a-new-website-within-the-multisite-and-set-the-language-for-the-site), and connect them in MultilingualPress through the _Relationships_ section.

If now we go to _MySites→Network Admin__→__MultilingualPress_ we see that the ACF Module is disabled.

[caption id="attachment_13615" align="aligncenter" width="975"][![ACF checkbox disabled](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_ACF_Module_Deactivated.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_ACF_Module_Deactivated.png) If ACF Plugin is not installed and activated the MultilingualPress module is disabled[/caption]

This because we haven't installed yet the ACF Plugin in the Network. To accomplish that let's proceed to the next section.

## ACF installation and activation

In this section, we can now proceed in installing the Advanced Custom Fields Plugin. To do so you can log into your WordPress installation back end and then go to _My Sites→Network Admin→Plugins_.

From there, search for _Advanced Custom Fields By Elliot Condon_ Plugin, then install and activate the Plugin by clicking on the button.

[caption id="attachment_13560" align="aligncenter" width="1897"][![ACF plugin download on wordpress.org](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/ACF_install_activate.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/ACF_install_activate.png) Download, install and activate ACF Plugin[/caption]

This way you activated the ACF Plugin on your site.

## ACF Module Activation

The next step is to activate the ACF module in MultilingualPress. This can be easily accomplished by going into _MySites→Network Admin_ and selecting the _MultilingualPress_ link in the left menu.

This way you access the MultilingualPress settings page. From there, in the _Modules_ tab, click on the _ACF_ checkbox and finally press the _Save Changes_ button to activate the ACF module.

[caption id="attachment_13612" align="aligncenter" width="1323"][![MultilingualPress Modules settings tab](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_ACF_Module_Activation.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_ACF_Module_Activation.png) ACF Module Activation in MultilingualPress[/caption]

## ACF Settings

In this section, we provide an example of how the custom fields should be set.

Suppose we want to add a proverb every time we create a post. To achieve that let's create a group of new custom fields to be added to the standard posts called _Proverbs Group_.

Go to your main subsite _Dashboard_ and then head to _Custom Fields→Add New._ Fill in the group text field the name _Proverbs Group_ as shown below.

[caption id="attachment_13618" align="aligncenter" width="1555"][![ACF Settings screen for group field creation](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Creating_New_Field_Group.png "Create a group field using ACF plugin")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Creating_New_Field_Group.png) Create a group field using ACF Plugin[/caption]

In the _Location_ section, it is possible to specify to which post type the new fields will be added.

Right under the Field Group name, it is possible to add one or more custom fields pressing the _Add Field_ button . Let's create a text area field with label _Proverb_ as shown below.

[caption id="attachment_13619" align="aligncenter" width="1889"][![ACF Settings screen to create a custom field](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Creating_New_Field.png "Create a custom field using ACF plugin")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Creating_New_Field.png) Create a custom field using ACF Plugin[/caption]

The ACF Plugin lets you configure several types of fields, for further details you can refer to the [official documentation](https://www.advancedcustomfields.com/resources/)

At this point the fields are ready in our main subsite, but now we also need to create **the same custom fields** in all the subsites where we want manage their translation through MultilingualPress.

To proceed, go to the main subsite _Dashboard_ and there head to _Custom Fields→Tools ._ In that section, it is possible to export the custom fields we want to replicate in other subsites.

Select the _Proverbs Group_ checkbox in the _Export Field Group_ meta-box, then press _Export File_ to create the file with the data to export.

[caption id="attachment_13620" align="aligncenter" width="1905"][![ACF exporting custom fields Tool](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/ACF_Exporting_Custom_Fields.png "Export the custom filed through the ACF Tool")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/ACF_Exporting_Custom_Fields.png) Export the custom filed through the ACF Tool[/caption]

Similarly, from the _Dashboard_ of a secondary sub-site related with the main one, the site _it_ in our example, import the previously exported file: head to _Custom Fields→Tools_ and in the _Import Field Group_ section upload the file and then press _Import File ._

[caption id="attachment_13621" align="aligncenter" width="1908"][![ACF exporting custom fields Tool](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/ACF_Importing_Custom_Fields.png "Import the custom filed through the ACF Tool")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/ACF_Importing_Custom_Fields.png) Import the custom filed through the ACF Tool[/caption]

At this point, we have the same custom fields in two subsites connected through MultilingualPress.

Finally let's check how MultilingualPress manages such fields.

## ACF Translation

At this point we are ready to work with the custom field through MultilingualPress.

To do so, let's create a new post in the main subsite and let's fill the _Proverb_ field with the sentence  "_You can lead a horse to water, but you can't make him drink._", as shown in the picture below.

[caption id="attachment_13622" align="aligncenter" width="1582"][![Post creation](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Creating_New_Post-_With_Custom_Field.png "Insert a proverb in a new post")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Creating_New_Post-_With_Custom_Field.png) Insert a proverb in a new post[/caption]

Then in the translation meta-box that relates the content with the connected subsite, _it_ in our example, we select the radio button option in order to create a copy of our post.

[caption id="attachment_13630" align="aligncenter" width="971"][![Translation meta box](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Translation_Box.png "Creating the post on the remote site via translation meta-box")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Translation_Box.png) Creating the post on the remote site via translation meta-box[/caption]

After this selection, the other tabs are enabled: we can access the _ACF_ tab and set the checkbox in order to overwrite the remote custom field content with the proverb sentence we previously inserted.

[caption id="attachment_13624" align="aligncenter" width="1101"][![Copy ACF field option on translation meta-box](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Translation_Box_Copy_Field.png "Copy ACF field option on translation meta-box")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Translation_Box_Copy_Field.png) Copy ACF field option on translation meta-box[/caption]

After that we can save our post and go to the second subsite, _it_ in our case. There we will find the new post created via MultilingualPress with the same custom field filled with the expected proverb content.

[caption id="attachment_13625" align="aligncenter" width="1581"][![Post duplicated on remote sub site](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Field_Overwritten_Translation_Post.png "In the remote sub site the post is duplicated and the custom field content is duplicated too")](https://multilingualpress.org/wp-content/uploads/sites/12/2020/09/MultilingualPress_Field_Overwritten_Translation_Post.png) In the remote subsite, the post is duplicated and the custom field content is duplicated too[/caption]

Similarly, you will be able to propagate any custom field content to all the related subsites. Just working only on a single post, all the related ones will be then properly managed by MultilingualPress.