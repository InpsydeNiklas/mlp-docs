In this tutorial we explain how you can install and set up a [WordPress Multisite](https://multilingualpress.org/wordpress-multisite-network/) to build a network of websites. We assume that you already installed a [WordPress Single Site](https://codex.wordpress.org/Installing_WordPress). Moreover we assume you have FTP access to the directory of your WordPress installation, as you need to change some files.

## Install WordPress Multisite - the Requirements

Before you start to install the WordPress multisite, please make sure that:

- You already have a WordPress installation
- [Pretty Permalinks](https://codex.wordpress.org/Using_Permalinks) are activated. This means your URLs should not look like this  _http://example.com/?p=2345_, but rather like this _http://example.com/my-page_
- All plugins are deactivated
- **Important:** you have a backup of your WordPress installation
- You have FTP access to your WordPress installation

## Allow Multisite in wp-config.php

The first step is to activate the Multisite feature in the file _wp-config.php_.

1. Set up a FTP connection to your website.
2. Open the file _wp-config.php,_ which is is located in the main directory of your WordPress, and add the line  
    `define('WP_ALLOW_MULTISITE', true);`  
    above the line:  
    `/* That's all, stop editing! Happy blogging. */`[caption id="attachment_1622" align="aligncenter" width="627"][![Define WP_ALLOW_MULTISITE in wp-config.php](https://multilingualpress.org/wp-content/uploads/sites/12/2018/04/wp-config-allow-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/04/wp-config-allow-multisite.png) Define WP_ALLOW_MULTISITE in wp-config.php to enable the Multisite feature.[/caption]
3. Save the file _wp-config.php_.

Now you enabled the Multisite feature in your WordPress installation. But you haven't finished yet. The next step is to install the network.

## Install the WordPress Network

1. Refresh the page in your browser and log in to your website.
2. In the left sidebar under _Tools_ you will find the menu tab _Network Setup_, where you can configure your WordPress Multisite.[caption id="attachment_1624" align="aligncenter" width="1101"][![Create a network of WordPress sites](https://multilingualpress.org/wp-content/uploads/sites/12/2018/04/create-wordpress-network.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/04/create-wordpress-network.png) Install a WordPress Multisite - Settings page "Create a Network of WordPress Sites"[/caption]
3. Decide whether you want to use subdomains for the sites in your network (e.g. _site1.example.com)_ or whether you want to have them installed in subfolders (e.g. e_xample.com/site1)_.  This setting affects all the sites in your network, you cannot change that later on.  Do you need a site to be mapped to a top level domain (e.g. _mydomain.com_)? This is possible with [domain mapping](https://codex.wordpress.org/WordPress_Multisite_Domain_Mapping).
4. Enter a name for your network in the field _Network Title_ in the section _Network Details_.  
    
5. Enter the site admin's e-mail address.
    
6. Click the _Install_ button.

## Add some code to wp-config.php and .htaccess

WordPress will now provide you with two snippets of code, which you need to add to the _wp-config.php_ and _.htaccess_ files. Both files are located in the root directory of your WordPress.

1. Set up a FTP connection to your website.
2. Add the first code snippet to your _wp-config.php_ directly above the line  
    `/* That's all, stop editing! Happy blogging. */`  
    The snippet looks like this, but adapted to your own site:
    
    define('MULTISITE', true);
    define('SUBDOMAIN_INSTALL', true);
    define('DOMAIN_CURRENT_SITE', 'My Website');
    define('PATH_CURRENT_SITE', '/');
    define('SITE_ID_CURRENT_SITE', 1);
    define('BLOG_ID_CURRENT_SITE', 1);
    
3. Add the second code snippet to the _.htaccess_ file and replace other WordPress rules.
    
    RewriteEngine On
    RewriteBase /
    RewriteRule ^index\.php$ - [L]
    
    # add a trailing slash to /wp-admin
    RewriteRule ^([_0-9a-zA-Z-]+/)?wp-admin$ $1wp-admin/ [R=301,L]
    
    RewriteCond %{REQUEST_FILENAME} -f [OR]
    RewriteCond %{REQUEST_FILENAME} -d
    RewriteRule ^ - [L]
    RewriteRule ^([_0-9a-zA-Z-]+/)?(wp-(content|admin|includes).*) $2 [L]
    RewriteRule ^([_0-9a-zA-Z-]+/)?(.*\.php)$ $2 [L]
    RewriteRule . index.php [L]
    
4. Save both files.

## Menu network administration and the network settings

When you changed the _wp-config.php_ and the _.htaccess_, log into your WordPress admin area again. In the upper admin bar, you now see the new menu N_etwork Admin._ It's displayed always, so you can always enter the admin area of the network, no matter on which site of your network you are. We take a look at the sub menues later on.

Below the network administration, all sites of the network are listed to which you were added. By clicking on the names, you enter the backends of these sites.

[caption id="attachment_1672" align="aligncenter" width="609"][![The menu Network Admin of a WordPress multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/network-admin-menu-wordpress-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/network-admin-menu-wordpress-multisite.png) The menu Network Admin of WordPress multisite[/caption]

And here's the explanation of the menu tabs in the network administration:

- **Dashboard**: Here you can find the widget to add new users and new sites to your network.
- **Sites**: On this tab, you can see all sites of your network - similar to the posts and pages. By moving the cursor over the websites, you see for example links to edit, display the dashboard, view, delete, archive or deactivate the sites. Note that you have fewer functions for the main page of your network, as this one always needs to exist and you cannot delete it.
- **Users**: Here you can administer the users of your network. In contrast to a single site installation, you can assign the super admin user role. The super admin has access to all sites and can make changes within the whole network. If you want a user to have access to the sites of your network, you need to add the user to each site via the user administration of the sites.
- **Themes**: The theme administration. Here you can install and uninstall themes and activate or deactivate them for the whole network.
- **Plugins**: Here you can find all installed plugins. You can add new plugins or delete them, you can activate or deactivate them for the whole network.
- **Settings**: On this tab you can find and edit the basic settings for your site, for example: the network name and the admin E-Mail address, you can allow user registrations, add new users to the site admins, you can make the themes and plugins menu available for site admins or set the standard language of your sites.

## Add a new website to the network

A WordPress multisite with only one website doesn't really make sense. To a WordPress multisite, you can add as many websites as you want - always and any time, so, it needn't be at the beginning. To enhance your website with a new site, take the following steps:

1. Go to M_y Sites_ _→ N__etwork Admin_ _→ S__ites_ and click _Add new_.[caption id="attachment_1673" align="aligncenter" width="732"][![Add a new website to a multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/add-new-site-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/add-new-site-multisite.png) Add a new website to a multisite[/caption]
2. Enter the desired website address. In this case, we decided for a network with sub directories. The domain is already given, we just add the sub diretory.[caption id="attachment_1674" align="aligncenter" width="911"][![Settings for the new website in the multisite network](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/settings-new-website-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/settings-new-website-multisite.png) Settings for the new website in the multisite network[/caption]
3. Define a title of the website. This one is displayed at several positions in your network, for example in the backend as website name in _My Sites_, but maybe also in the frontend or in meta data like the page title.
4. Choose a language for the new website.
5. Choose the admin e-mail address which must be different than the one for the whole network. If there is no user with this e-mail yet, a new user with admin role for this site will be created.
6. Click the button _Add Site_. Your new site is to be created and will be displayed in M_y Sites_  _→ Network Admin_ _→ Sites__._ However, in order to let others than the current admin administer this new site, you need to add them as user with admin role to this site.

## Install Plugins and Themes in the WordPress multisite

Install or uninstall plugins or themes in a WordPress multisite network is something only the super admin can do. The site admins within the network can only activate or deactivate them. Well, and site admins can only activate and deactivate plugins in case the super admin checked the box _Enable administration menus_ in the network administration in S_ettings_ _→ Network Settings._

[caption id="attachment_1680" align="aligncenter" width="978"][![Enable administration menus](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/multisite-network-settings-enable-admin-menus.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/multisite-network-settings-enable-admin-menus.png) Enable administration menus to allow admins to enable/disable plugins.[/caption]

You can find the plugins administration for the whole network under N_etwork Admin_ _→ P__lugins_, the themes administration under N_etwork Admin → Themes._

[caption id="attachment_1681" align="aligncenter" width="1029"][![Install plugins in a multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/insta-plugin-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/insta-plugin-multisite.png) Install plugins in a multisite and make them available for the whole network[/caption]

For the site admin, the whole thing looks like the next picture.

[caption id="attachment_1682" align="aligncenter" width="824"][![The plugins administration as site admin in a WordPress multisite](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/plugin-admin-wordpress-multisite.png)](https://multilingualpress.org/wp-content/uploads/sites/12/2018/05/plugin-admin-wordpress-multisite.png) The plugins administration as site admin in a WordPress multisite[/caption]

Hint: The admin can activate and deactivate plugins, but he cannot install or uninstall them.

For one of the plugins in our example you can read _Network Only_. This means the plugin is available only for all sites or for no site. Moreover, it's the super admin only who can set the settings of this specific plugin, you need to make them in the network administration.

You can find further help to set up your multisite in our documentation category [WordPress Multisite 1x1](https://multilingualpress.org/docs-category/wordpress-multisite-1x1/). In case you are setting up a multilingual website, take a look at: [MultilingualPress getting started](https://multilingualpress.org/docs-category/getting-started/).