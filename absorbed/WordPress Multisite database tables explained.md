Working with a WordPress Multisite requires a little bit more knowledge about WordPress and experience as WordPress admin than working with a single site. When you try to fix problems with your WordPress Multisite network, it is sometimes helpful to know how the database of a multisite is structured and what the differences between a Single Site database and a WordPress Multisite database are.

So let's take a look to which database tables do we have in a single site and which we have in a multisite. We will briefly explain each of the multisite specific tables. If you need an explanation of single site tables, please read the post [Database Description](https://codex.wordpress.org/Database_Description) in the WordPress Codex.

Hint: Starting from a single site WordPress installation it is possible to switch to a WordPress Multisite through a procedure as described in the [WordPress codex.](https://codex.wordpress.org/Create_A_Network)

## WordPress single site database tables

In a single site WordPress installation the database tables used are:

- _wp_commentmeta_
- _wp_comments_
- _wp_links_
- _wp_options_
- _wp_postmeta_
- _wp_posts_
- _wp_terms_
- _wp_termmeta_
- _wp_term_relationships_
- _wp_term_taxonomy_
- _wp_usermeta_
- _wp_users_

After we proceed with the Multisite install procedure, some of these tables are updated and other new tables are added. The remaining ones are not changed but they start to refer to the main site, while for other sites (not the main) specific ones are created.

## WordPress Multisite database tables

So here the new situation after a Multisite install:

- _**wp_blogs → NEW**_
- _**wp_blogs_versions → NEW**_
- _wp_commentmeta **→ refers to main site**_
- _wp_comments **→ refers to main site**_
- _wp_links **→ refers to main site**_
- _wp_options **→ refers to main site**_
- _wp_postmeta **→ refers to main site**_
- _wp_posts **→ refers to main site**_
- _**wp_registration_log → NEW**_
- _**wp_signups → NEW**_
- _**wp_site → NEW**_
- _**wp_sitemeta → NEW**_
- _wp_terms **→ refers to main site**_
- _wp_termmeta **→ refers to main site**_
- _wp_term_relationships **→ refers to main site**_
- _wp_term_taxonomy **→ refers to main site**_
- _**wp_usermeta**  **→ UPDATED**_
- _**wp_users  → UPDATED**_
- **SITE SPECIFIC TABLES → NEW, refers to other site(s) except the main one**

### New tables

- _**wp_blogs:** each site created is stored in that table_
- _**wp_blogs_versions:** this table keeps track of the datadase version status for each site_
- _**wp_registration_log:** in this table is stored the admin user created when a new site is created_
- _**wp_signups:** in this table are stored the users that have registered for a site via the login registration process._
- _**wp_site:** in this table is stored the sites address_
- _**wp_sitemeta:** here are tracked various site informations_

### Updated tables

- _**wp_users:** the list of all users of all the sites is maintained in this table_
- _**wp_usermeta:** here are stored the meta data of users for all the sites_

### Site Specific Tables

The data of the main site is stored in existing unnumbered tables, while the data of additional sites is stored in new numbered tables.

So for the main site we have these dedicated tables:

- _wp_commentmeta_
- _wp_comments_
- _wp_links_
- _wp_options_
- _wp_postmeta_
- _wp_posts_
- _wp_terms_
- _wp_termmeta_
- _wp_term_relationships_
- _wp_term_taxonomy_

While, for example, when a new site is created, the site-specific tables, similar to the single site install, are created. Each set of tables for a site is created with the site ID (blog_id) as part of the table name. These are the tables that would be created for site with ID 2 :

- _wp_2_commentmeta_
- _wp_2_comments_
- _wp_2_links_
- _wp_2_options_
- _wp_2_postmeta_
- _wp_2_posts_
- _wp_2_terms_
- _wp_2_termmeta_
- _wp_2_term_relationships_
- _wp_2_term_taxonomy_

**References:**

[**https://codex.wordpress.org/Database_Description**](https://codex.wordpress.org/Database_Description)

[**https://deliciousbrains.com/wordpress-multisite-database-tour/**](https://deliciousbrains.com/wordpress-multisite-database-tour/)

[**https://rudrastyh.com/wordpress-multisite/database-tutorial.html**](https://rudrastyh.com/wordpress-multisite/database-tutorial.html)