When you need to build a network of related sites, to choose whether rely on different single site WordPress installations, or on a [WordPress Multisite installation](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/), is not a trivial issue. In fact there are many aspects you need to consider.

Here follow several pros and cons of using a WordPress Multisite installation to build your site network.

## The Pros of a WordPress Multisite

- Manage all sites from the same dashboard, through a single Super Admin user.
- The site administrator cannot install or change plugins and themes, only the Super Admin can do this. This lets you more control and avoids conflicts, keeping control centralized.
- You need to install themes and plugins only once and then you can activate them across the entire network. Also you execute the upgrade process only once.
- Store all sites data in a single backup, no need to backup each site.
- Since every WordPress installation takes a considerable amount of resources on the server, using a Multisite installation you don’t spend so much resources (and money) and the optimization process can be less painful.
- You can properly configure and maintain multilanguages versions of the same site through a multisite structure and [multi languages plugins](https://multilingualpress.org).

## The Cons of a WordPress Multisite

- Not all plugins work on multisite. Usually most plugins are basically created for single site and this can lead to conflicts.
- Individual site administrators cannot install/uninstall plugin and themes, this limits site administrators power.
- A hacker attack or just a downtime on your server will affect all the sites.
- A data breach will involve all the data of all the sites.
- Big traffic on one site may affect the speed of all the other sites of the network, for bandwith reason but also because all sites share the same database.
- Not all hosting plans support multisite.
- If you need to keep users on separated sites, Multisite can lead to security risk, due also to eventual leaks in plugins/themes.
- If a theme or a plugin is updated, it is updated for all sites of the network that use it. Change versions between sites could be complicated.
- If the number of sites increases, to manage it within a multisite installation could be critical.
- There could be some reasons that make you want to change a multisite installation into different single sites installations: for example if one site becomes too big, or just the number of sites increases too much making the whole system slow. To switch from multisite installation back to single site is hard to achieve.
- In case of testing new plugins/themes features, for a single site administrator is difficult to work because he cannot activate/deactivate or install/delete it since this can be done only through the Super Admin user.
- All sites share the same user profiles. You cannot create for example the same user two times for two different sites on the network. Besides logged in users are logged in for all sites.

**Further reading about WordPress Multisite Pros and Cons:**

wpexplorer.com - [Pros and Cons of WordPress Multisite – How to Install Multisite With Local Xampp](http://www.wpexplorer.com/pros-cons-wordpress-multisite/)

Quora - [Are there any disadvantages to using WordPress Multisite?](https://www.quora.com/Are-there-any-disadvantages-to-using-wordpress-Multisite)

narga.net - [WordPress Multisite vs Multiple WordPress Installations](https://www.narga.net/wordpress-multisite-versus-multiple-wordpress-installations/)

wpmudev.org - [Multisite Pros & Cons](https://premium.wpmudev.org/forums/topic/multisite-pros-cons)