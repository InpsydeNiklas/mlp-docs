You wonder what the WordPress multisite is about? With our WordPress multisite overview, we want to give a first impression about the WordPress multisite feature.

You can find even more details in the category [WordPress Multisite 1x1](https://multilingualpress.org/docs-category/wordpress-multisite-1x1/) in our MultilingualPress documentations. As a beginning, we recommend our post [Install and Set up WordPress Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/).

## What's the WordPress Multisite? - A Network of Websites

The multisite is a WordPress feature with which users can create a **network of websites** in a single WordPress installation. This way, users can administrate websites professionally.

Multisite is available since WordPress 3.0 and was created out of  [WPMU](https://codex.wordpress.org/WPMU) (WordPress MultiUser).

The great thing about a WordPress multisite is the fact that it looks very similar to a standard installation. The multisite installation has the same folder structure, the same basic files and the same code base. That's what makes the installation of a multisite network nearly as easy as the installation of a standard WordPress site (WordPress Single Site). And updates of a multisite are a piece of cake, too.

## Single Site and Multisite: The Differences

However, there are some differences between a WordPress Single Site and a Multisite . There are differences between the admin screens and their usage, between the files in your WordPress installation and between the database files.

### Admin Screens

As soon as you activated the multisite, you see some more screens in the admin area to administrate the network.

[caption id="attachment_1823" align="aligncenter" width="919"][![WordPress Multisite Overview - Multisite Admin Dashboard](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/wordpress-multisite-overview.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/wordpress-multisite-overview.png) WordPress Multisite Overview - Multisite Admin Dashboard[/caption]

Only Super Admins see this admin area. They can install themes and plugins and create and administrate sites. Besides to the role Super Admin, you can assign the role "standard" admin for admins of websites within the network. Owners of this role cannot install themes and plugins but can only activate those which were installed within the network.

### Files

The only differences between files of the standard WordPress installation and the multisite installation are those of the _wp-config.php_ file, the ._htaccess_ file and the _wp-uploads_ folder. As soon as you installed the multisite network, there are a few more lines of code in the _wp-config.php_ file, which tell WordPress how to run. The _wp-uploads_ folder contains, in a WordPress multisite installation, sub folders for each single website. Files which have been uploaded to the websites are stored in the corresponding folder - with the same structure you have in the _wp-uploads_ folder of the standard installation.

### Database

The database of a standard WordPress installation contains of twelve database tables in which the page content and the settings are stored. In a multisite network, ten of these tables are duplicated for each website. This means: The more websites in the network, the more database tables. They separate the content of each website within the multisite network.

## Overview of Multisite Features

- You can create a network with a couple of blogs and websites out of only one single WordPress installation.
- Moreover you can have a network of subdomains like _http://multisite.domain.com_ or directories like _http://www.domain.com/multisite/_ or have top level domains.
- Open a WordPress multisite network for other users to create accounts and blogs.
- All themes and plugins are stored only once - independent from the number of websites on which you use them. This means that you need less server space than with a WordPress installation of each website.
- There is the role of the Super Admin who is admin of the whole network and the website administrator role who administrates only one website within the network. As Super Admin, you can install themes and plugins and all admins of the websites within your network can activate them. Website administrators within the network don't have the permission to install themes or plugins.
- As Super Admin, you can make changes of the themes for all websites. Website administrators cannot change anything concerning the theme.
- Create websites and shops for a couple of languages, regions, currencies and so on. The best plugin to use for multilingualism in WordPress is the plugin [MultilingualPress](https://multilingualpress.org), which is used with a WordPress multisite.

Well, all this means that different websites may have the same design - or not. It's the Super Admin's decision what kind of themes and plugins are available for the website administrators to design their websites. With the help of MultilingualPress you can build a multilingual network of websites which are more or less different: the same or a different design, the same or different features, completely different content or just a few different words, different products or just another currency.

## WordPress Multisite Overview - Use Cases and Examples

A multisite network has many use cases. For example you can use it to create a network of websites or blogs for several people or a whole company. Moreover, agencies or developers can use the network to keep the customer websites they install and administrate at one place.

**An example for the usage of WordPress multisite:** A building materials company has a couple of stores with different corporate identities in an umbrella brand.  There, the company's head quarter could make the administration of the whole WordPress installation, while each store can work on its own website within the network. Of course, each website can have the same elements to comply with the corporate design. The head quarters would do the WordPress updates and install plugins both for all websites and individual store requests. You can transfer similar approaches to universities with international focus: With the WordPress multisite, they can have multilingual websites in one installation. The use cases for the WordPress multisite feature are quite diverse.

Here some examples:

1. **Inpsyde.com**  - multilingual website[caption id="attachment_1817" align="aligncenter" width="1366"][![WordPress Multisite Overview - example inpsyde.com](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/inpsyde-mlp.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/inpsyde-mlp.png) WordPress Multisite Overview - Example inpsyde.com[/caption]
2. **Multilingual online shop of Vectorcam**[caption id="attachment_1819" align="aligncenter" width="1366"][![WordPress Multisite Overview - Example Vectorcam](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/vectorcam.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/vectorcam.png) WordPress Multisite Overview - Example Vectorcam[/caption]
3. **Inpsyde product pages** backwpup.com, backwpup.de, multilingualpress.de, and multilingualpress.org - here we have different products and different languages in one installation[caption id="attachment_1821" align="aligncenter" width="1366"][![WordPress Multisite Overview - Example Inpsyde Product Pages](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/mlp-english.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/mlp-english.png) WordPress Multisite Overview - Example Inpsyde Product Pages[/caption]

However, there are some use cases in which the multisite isn't the best solution. For example, if you're not planning to have more than one website. Or in case you create several websites but your customers have different hosters.

Our WordPress multisite overview was convincing? It's exactly what you need? Then just start with the installation. Here you can find the [tutorial how to install and set up a WordPress multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/).