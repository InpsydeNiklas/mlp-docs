In this document, we'll explain how to translate custom fields using MultilingualPress. For the sake of simplicity, we are going to use the [Advanced Custom Fields](https://wordpress.org/plugins/advanced-custom-fields/) Plugin to create the custom fields. Just keep in mind that the process described here is the same for any other Plugin that allows you to create custom fields or if you are creating them manually using [WordPress Custom Fields API.](https://wordpress.org/support/article/custom-fields/)

**Note:** MultilingualPress offers since version 3.5.0 full compatibility for Advanced Custom Fields. Therefore, Advanced Custom Fields can also be translated for connected pages within the WordPress editor. Here is a special [Tutorial for translating Advanced Custom Fields](https://multilingualpress.org/docs/how-to-translate-advanced-custom-fields-acf-with-multilingualpress-3/) explaining all functions.

There are currently two approaches about how to implement custom field translations.

## Creating a new site based on an existing one

The first one is setting up the main site, create the custom fields and the content. Once everything is created we can create a new site based on the existing one. Doing so will copy everything to the new site and we are only going to need to translate the content. Everything else including the custom fields will be automatically created in the new site.  
Here is a quick video showing the process of creating a new site based on an existing one with existing custom fields:  

[video width="1372" height="752" mp4="https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/create-site-custom-fields.mp4"][/video]

## Creating the custom fields manually in each site

The second approach is when you already have two or more sites connected and you want to include custom fields. In that case, the custom fields need to be created manually on each site.

In this article, we are going to explain the second approach. To do so we´ll create a new WordPress Multisite installation with two sites connected:

[caption id="attachment_11143" align="aligncenter" width="1258"][![Two connected sites in a multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/connected-sites-in-multisite.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/connected-sites-in-multisite.jpg) Two connected sites in a multisite using MultilingualPress 3[/caption]

### Install and Network activate Advanced Custom Fields

[caption id="attachment_11144" align="aligncenter" width="1256"][![Install Advanced Custom Fields](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/install-advanced-custom-fields.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/install-advanced-custom-fields.jpg) Install the Plugin Advanced Custom Fields[/caption]

Go to _My Sites -> Network Admin -> Plugins_ and install _Advanced Custom Fields_. In this case, we are network activating it, that decision will depend on the nature of each Plugin if it includes support for Multisite or not. If you are in doubt, the recommended way is to activate individually on each site, like you usually do in a single site.

### Create a custom field in the main site

[caption id="attachment_11145" align="aligncenter" width="1263"][![Advanced Custom Fields UI - create new group and a field](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/create-field-acf.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/create-field-acf.jpg) Advanced Custom Fields UI - create a new group and a field[/caption]

In site 1 create a new group and a new field using _Advanced Custom Fields UI_.

[caption id="attachment_11146" align="aligncenter" width="1260"][![Set value of the custom field in a post](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/value-of-custom-field.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/value-of-custom-field.jpg) Set value of the custom field in a post[/caption]

In site 1 fill the value of the custom field in a post.

### Create the custom field in site 2

In order to create the custom fields in site 2, we can use the export/import functionality provided by Advanced Custom Fields on the Tools page. But because in our example we are only dealing with one single group with one single field, we are going to create it manually in site 2.

[caption id="attachment_11147" align="aligncenter" width="1490"][![Create the custom field in site 2](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/create-field-acf-2.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/create-field-acf-2.jpg) Create the custom field in site 2[/caption]

The most important thing to keep in mind here is to ensure that the field slugs are exactly the same across all connected sites. That way the code displaying the fields will grab the correct translation based on the site the visitor is currently in. So let's say that you create a new field with the slug ‘some_field’ on site 1, you need to create a field with the same exact slug ‘some_field’ in site 2.

### Connect the posts that contain the custom fields

[caption id="attachment_11148" align="aligncenter" width="1493"][![Connect the posts with custom fields](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/connect-posts.jpg)](https://multilingualpress.org/wp-content/uploads/sites/12/2020/03/connect-posts.jpg) Connect the posts with custom fields[/caption]

Finally, in order to be able to connect custom fields across sites, you simply need to connect the posts containing the fields using MultilingualPress translation metabox.