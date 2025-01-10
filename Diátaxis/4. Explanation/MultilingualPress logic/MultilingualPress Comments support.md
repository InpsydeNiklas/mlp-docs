Starting from version 4.2.0 of MultilingualPress, a module is available to manage the content related to comments in the same way the plugin manages the relationships between various post types (posts, pages, taxonomies, custom posts, WooCommerce products).

## Module activation

To activate the module, follow the usual procedure by accessing the [settings of MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress/#Global-settings-for-MultilingualPress) and activate the respective module as shown in the figure below:

[caption id="attachment_26028" align="aligncenter" width="738"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Global-settings.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Global-settings.png) MultilingualPress Global Settings - Enabling comments module[/caption]

At this point, let's assume that we have two sites in our Multisite network, for example, one in English and one in Italian, and they have been previously connected using MultilingualPress.

On the first site, let's create a post titled "First Post English Site." Using the MultilingualPress translation meta box, we can quickly create a copy of this post in the Italian version site: let's name it "First Post Italian Site."

We now have two posts that are related to each other through MultilingualPress. If the posts are published, they will be visible on the front end. Additionally, when users access them, they can leave comments (assuming comments are enabled).

If a comment is added to the English post "First Post English Site”, for example, we can access the WordPress backend and select the "Comments" option from the left menu. The created comment will be visible here. Select the link to edit the comment, as shown in the picture below.

[caption id="attachment_26029" align="aligncenter" width="1470"][![Edit comme](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Comment-edit.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Comment-edit.png) Edit comment[/caption]

A translation box is displayed below the comment. Like with the posts, this box allows you to associate the source comment with another comment on the Italian site. Of course, to be associated, both comments must be related to connected posts through MultilingualPress. The related comments cannot be connected via MultilingualPress if the posts are not connected.

[caption id="attachment_26030" align="aligncenter" width="1424"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Comment-with-translation-metabox.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Comment-with-translation-metabox.png) Comment with translation meta box[/caption]

As seen in the image above, the translation meta box for comments is similar to the ones used for posts. It allows you to create a copy of the source comment, establish a relationship with an existing comment, or remove a relationship if one already exists.

Let's proceed by selecting the second option to create a new comment for the Italian version of the post. Then, by clicking on the "Content" tab, we find additional fields to specify our comment  further, as shown below:

[caption id="attachment_26031" align="aligncenter" width="1405"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Translation-meta-box-content.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Translation-meta-box-content.png) Translation meta box - content[/caption]

In our example, let's select the option "_Overwrite all the translated author field values with the ones from source._" By doing so and saving our changes, the new comment on the Italian site will have the same content as the source comment related to the English site.

## Comments bulk copy

Suppose you want to copy all comments from one site to another, or automatically create a comment on another site as soon as the source comment is created. In that case, this is still possible through the settings panel provided by MultilingualPress for each subsite of the multisite network.

Suppose, for example, that our two sites, English and Italian, are already connected through MultilingualPress, and have a post associated with each other through MultilingualPress. In the previously described example, we have precisely such a case: "First Post English Site" and "First Post Italian Site" are linked.

Suppose the post on the English site receives several comments and you intend to transfer those comments to the Italian version as well. In that case, you simply need to access MySites->NetworkAdmin->Sites, then select the site from which you want to copy the comments: the English site.

This way, we access the settings page where we select the "MultilingualPress - Comments" tab, as shown in the following image:

[![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Bulk-copy-comments.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Bulk-copy-comments.png)

On that page, in the "post" section, under the title "_Copy comments to selected sites_" we select the option "Italian" and press the "_Save Changes_" button. This way, all the comments from the English site will be copied to the Italian site. As a result, all the comments from the post on the English site will now be visible in the corresponding post on the Italian site.

In case you don't want to align the comments this way, you can also select the "Italian" site under the title "_Create comments on selected sites when a new comment is added_": by doing so, if a user, for example, creates a new comment on the English site, this will be automatically created for the connected post on the Italian site as well.

The properties just described can be enabled not only for posts, but also for pages. You can set the different options in the "_page_" section to activate them appropriately.

## Creating a site as a copy of another

The MultilingualPress feature that allows [creating a new site as a copy of another](https://multilingualpress.org/docs/getting-started-with-multilingualpress/#Create-a-new-website-within-the-multisite-and-set-the-language-for-the-site), has been extended to include an option for copying comments as well. 

This way, creating a new site using an existing site as a template, including all its related comments, is possible.

In the image below, we highlight the newly introduced option.

[![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/BasedOn.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/BasedOn.png)

## WooCommerce Reviews

The new feature allows for similar management of product reviews in WooCommerce in addition to managing WordPress comments. This applies to WooCommerce stores connected within the multisite network using MultilingualPress.

Let's see an example. Make sure you have WooCommerce installed and activated in your multisite network. After activating the WooCommerce module in the [global settings of MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress/#Global-settings-for-MultilingualPress) and enabling "Products" in the corresponding post types tab, let's create a WooCommerce product on the English site. 

Next, let's create a review, comment and rating for that product.

By accessing the product in the backend, you can use MultilingualPress's translation meta box to create a copy of the product on the Italian site.

After performing this operation, when accessing the review in the editing mode of the English site, we can see that a translation meta box is now available, as shown in the following image:

[caption id="attachment_26034" align="aligncenter" width="1366"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Review-translation-meta-box.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Review-translation-meta-box.png) Review - Translation meta box -Relationship[/caption]

The corresponding "Content" tab, enabled when we select one of the available options to connect the comment, allows us to specify the review rating and the usual comment parameters.

[caption id="attachment_26035" align="aligncenter" width="1346"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Translation-meta-box-Review.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Translation-meta-box-Review.png) Review - Translation meta box - content[/caption]

Once the module that allows the management of the WooCommerce Product post type is activated, we also notice that in the bulk comments copy settings panel (see paragraph _Comments bulk copy_), a new section is available to copy and/or keep the reviews of the various products aligned, which are related through MultilingualPress.

These options are displayed in the image below.

[![](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Bulk-copy-reviews.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2023/05/Bulk-copy-reviews.png)