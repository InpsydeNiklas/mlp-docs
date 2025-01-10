This MultilingualPress tutorial is intended to quickly show to content authors how to create and update the content in a Multilingual site.

So we describe some common tasks focusing on the authors activities and not on the administration tasks of the Multisite Network and/or the MultilingualPress settings and configuration.

We assume instead that these kind of configuration is already properly set in the environment you are going to use.

For more info about these topics, you can refer to our docs: [Getting started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/) and [MultilingualPress – Common Questions & Answers](https://multilingualpress.org/docs/multilingualpress-3-common-questions-answers/)

## Routine activities in MultilingualPress

An author can normally deal with these routine tasks:

1. Publish new content with related terms (categories and tags)
2. Publish translations for that new content and terms in the available languages

Here we want to provide an example that shows how to perform such tasks. To do that we refer to a Multisite environment with 3 language sites: English, Italian, German.

Being this an example, we will not go through every detailed feature and configuration that MultilingualPress offers. These info are already available in the above links.

Instead we want to guide an Author describing some basic steps he should perform, in order to understand how MultilingualPress works and how to continue further to exploit all the power that the plugin and the Multisite Network can unleash.

Let's see how to create some content and manage the related translation in the following sections.

### Publish new content

Suppose we need to create a new blog post in our main English site.

That operation is really straightforward, since you can perform it as usual, like in a standard WordPress site.

In fact, just log into the English version site back end, then in the left menu head to _Post -> Add New_ .

There you can work on the content, create tags and/or categories, as usual.

After all of the content is provided we can focus on the translation part.

You can manage that by the so called translation metaboxes: just have a quick look at them in your post edit page, scrolling down the page to the bottom.

There you will find one language metaboxes for each language site you have connected. So, in our example 2 language metabox: one for the German site and another one for the Italian site translation, as shown in the picture below.

[caption id="attachment_15599" align="aligncenter" width="557"][![Post translation](https://multilingualpress.org/wp-content/uploads/sites/12/2021/01/Post-Translation-Metabox.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/01/Post-Translation-Metabox.png) Post Translation Metaboxes[/caption]

Similarly, after creating a tag and a category in order to associate them to your post, open them in edit mode, and you will find again at the bottom of the edit page the metaboxes needed to properly manage the terms translation.

Check the images below for the  categories and tags metaboxes.

[caption id="attachment_15600" align="aligncenter" width="822"][![](https://multilingualpress.org/wp-content/uploads/sites/12/2021/01/Categories-and-Tags-Translation-Metaboxes.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2021/01/Categories-and-Tags-Translation-Metaboxes.png) Categories and Tags Translation Metaboxes[/caption]

Through this metaboxes is possible to easily manage the translation.

Let's have a look in the next section of this MultilingualPress tutorial how this can be accomplished.

### Publish translation

In the previous section we created a post in the English site version and created also one  (or more) categories and tags that have been set for the post.

Now we want to create the translations for the Italian and German version site.

This can be achieved in different ways: MultilingualPress is very flexible and many tasks can be performed in different ways.

Here we show one of this way, but as soon as you get more confidence with the Multisite environment and with MultilingualPress you will be able to find your own way for manage the translation in your sites.

#### Translate Categories and Tags

For the moment so, we first proceed in translating the category.

Go in the category edit page and then in the metabox select "_Create a new term, and use it as translation in Italiano_" . Then select the "_Term_" tab, and fill the name of the translated category.

Perform the process again also for the German metabox and finally press the _Update_ button.

This way a category will be created in the Italian and the German sub sites, as a translation of the main one you are updating in the English version site.

Repeat all this process for the tag, since the process is the same: open it in edit mode and create the translations through the metaboxes.

#### Translate your post

Now go back to the post created in the English site, and scroll the page to reach the translation metaboxes.

Here, in Italian translation metabox select "_Create a new Post, and use it as translation in Italiano (Italia)_". After that several tabs are available. For each of them perform the action as explained here below:

- **Title and Content**: fill the "_New post title_" field, and in case you need, select the checkbox: this way the English text will be duplicated in the Italian site. This could be useful in case you want to perform the translation in Italian later, having the original text available in the same post
- **Advanced**: in the new post status select "_Publish_"; this way on the Italian site you publish the post directly with the English text
- **Taxonomies**: in this section select the checkbox for the category and the tag translated as explained in the previous section

Now that you set the requested data in the Italian translation metabox, proceed similarly with the German metabox too. Finally press the _Update_ button.

This way a new post is created in each site: the Italian and German one. The English text is the content set for all the post, while the category and tag are properly translated.

These post will be all in published status.

The next step will be to log into the Italian and German sub sites to provide the actual translations. For example log into the Italian back end, select the new post you created and replace the English content with the actual Italian content, as needed.

Finally update your posts: the Italian and German translation are now published.

We reached to goal of this MultilingualPress tutorial for authors.

### How to go further?

What we saw is a very simple example of what is possible to achieve with MultilingualPress. But there are many more options available.

For example, consider the activation of the _Quicklinks_ in the [MultilingualPress settings](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/#Global-settings-for-MultilingualPress-3) in order to have always a link in the post that let you easily navigate from a language site to another.

Also be aware that we created this example starting to work on the English site, but this was just a casual choice. In fact you can get the same results working first on the Italian or the German site.

Practice is the best way to master the Multisite environment and the MultilingualPress features, so go on trying, and check also all the info provided in our official documentation [here](https://multilingualpress.org/docs-category/multilingualpress-3/).