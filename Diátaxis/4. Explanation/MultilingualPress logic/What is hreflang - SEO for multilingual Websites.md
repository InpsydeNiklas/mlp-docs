In this tutorial we explain the link attribute rel=”alternate” hreflang=”x”. Moreover we focus on the relationship of hreflang, SEO and multilingual websites. Last but not least we show how to implement it with MultilingualPress.

### What is hreflang?

The link attribute **rel=”alternate” hreflang=”x”** is inserted into the website's head. Due to that search engines understand they shall show the users' preferred language. Moreover they learn that the website content is available in several languages.

**Example:**

<link rel="alternate" hreflang="en-US" href="https://syde.com">

The example displays that the current content is also available in the language version en-US on the page _https://syde.com_.

### Which impacts does hreflang have on SEO?

On the one hand the link attribute tells a search engine that a website's content is available in several languages. Thanks to that, the search engine can display the user's preferred language. On the other hand the attribute prevents a punishment due to duplicate content, for example when there is the same content for several languages/regions.

**Example:**

Company A has a multilingual website with contents for Germany, Switzerland and France. The contents of the Swisse and German website are partly identic. As both languages are quite similar, there would be a duplicate content problem without hreflang. But with the link attribute the search engine recognizes that it's content for different regions.

### How do I have to implement hreflang?

In case you have a number of language versions of one URL, each version needs to have a rel="alternate" hreflang="x" link both for itself and the other language versions.

**Example:**

When you offer content in German, English, and French, the German version needs to have a rel=”alternate” hreflang=”x” link attribute for itself additional to the links for the English and French language versions. The English and French versions need to refer to the French, English, and German language versions as well.

### How do I set up hreflang with MLP?

You need to connect the different languages for each website. As soon as you defined the translation relationships, MultilingualPress inserts the link attribute into the sites automatically.

Example of our own website https://multilingualpress.de:

[caption id="attachment_1115" align="aligncenter" width="1331"][![hreflang attribute for language or region URL](https://multilingualpress.de/wp-content/uploads/sites/16/2017/08/2018-01-14_13-43-55.png)](https://multilingualpress.de/wp-content/uploads/sites/16/2017/08/2018-01-14_13-43-55.png) hreflang attribute for language or region URL[/caption]

### How can I test whether hreflang is implemented correctly?

The website [sistrix.com](https://www.sistrix.com/hreflang-guide/hreflang-validator/) offers a hreflang validator.

Moreover the [Google documentation](https://support.google.com/webmasters/answer/189077?hl=en) offers further information.