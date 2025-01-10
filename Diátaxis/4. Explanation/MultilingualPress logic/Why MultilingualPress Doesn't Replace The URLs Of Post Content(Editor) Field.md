MultilingualPress is not a copying plugin. While it has all the features that help make website translations easier, it doesn’t translate any content, including the URLs.

When you copy content from the main post to the target language, MultilingualPress creates connections but does not automatically translate texts and content.

You can either translate the text and content manually or use translation services like Google Translate, Loco Translate, Eurotext, DeepL, and many more.

Luckily, MultilingualPress now offers an automatic translation add-on called the [WP Auto Translate](https://bit.ly/3O7uM6N) that automatically translates your content through translation services.

The WP Auto Translate add-on automatically translates the entire website content, including:  

- Post/page/custom post types, such as, title, **URL slug**, excerpt, and content.
- WordPress category/tag/taxonomy includes title, **URL slug**, and description.

## **Why MultilingualPress does not replace URLs?**

There are a few reasons why MultilingualPress doesn’t translate and replace post URLs when connecting sites and pages. Here are some of them:

#### **No connected post on the target site**

Unfortunately, some issues will surface if we decide to change or replace the URLs of the post_content field when connecting one post to another.

For example, if we set a URL in the post content related to a page in the source site, like _example.com/en/post-slug_, then changing the base URL to _example.com/de/post-slug_ for a German site would not work because the page with the post-plug may not exist on the _example.com/de_ site.

#### **Broken external link**

There’s no way to identify whether the URL in the post_content field belongs to the website or an external source. 

Moreover, translating and changing the external link might make the link and connection broken and inaccessible.

#### **Site performance issues**

The post editor field is just a meta saved in the website database as a single value. To change the URLs, we will need to run some regex queries to grab the URLs from the post.

Meanwhile, a single post can contain 1000 or more URLs. This means that even after obtaining the URLs, we will need to get the post object and check if it’s connected with the remote post, which might slow down the performance of your website.

#### **Broken media link**

Another issue that might surface if we automatically translate the URLs of the Post Content Editor field is the broken media links of the posts and content.

Since WordPress links have specific structures, replacing the media URLs can make the media inaccessible or even not show up on the connected posts.

Please check our documentation for more detailed and complete information on how to use MultilingualPress, or contact our support team.