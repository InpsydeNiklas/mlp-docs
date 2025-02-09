# Understanding the WordPress Multisite Database Structure

**Purpose**: This document explains _how_ WordPress Multisite modifies the standard WordPress database structure to accommodate multiple subsites within a single installation. By seeing _which tables are added or changed_, you can better understand how content, user data, and network settings are organized under the hood—and troubleshoot issues more effectively when they arise.

---

## Single-Site vs. Multisite Overview

In a **single-site** WordPress installation, you’ll typically see 12 default tables, each handling different aspects of site data (e.g., posts, users, comments). When you enable **WordPress Multisite**, a new “network” layer is introduced, and WordPress **duplicates certain tables** for each subsite—while also creating several _network-level_ tables for global settings and relationships.

### Core Single-Site Tables

A standard single-site WordPress includes the following tables (prefix may vary, e.g., `wp_` is default):

1. `wp_commentmeta`
2. `wp_comments`
3. `wp_links`
4. `wp_options`
5. `wp_postmeta`
6. `wp_posts`
7. `wp_terms`
8. `wp_termmeta`
9. `wp_term_relationships`
10. `wp_term_taxonomy`
11. `wp_users`
12. `wp_usermeta`

Upon converting to or installing a multisite, some of these tables become **network-aware**—particularly `wp_users` and `wp_usermeta`, which turn into global user tables shared by every subsite.

---

## New and Updated Tables in Multisite

When you activate Multisite, WordPress adds **network-level** and **multisite-specific** tables, plus _duplicates_ existing site tables for each new subsite.

### Network-Level Tables

1. **`wp_site`**
    
    - Stores high-level information about the network itself. In WordPress core, only one “site” (the network) is typically used, but the structure supports multiple networks via plugins like WP Multi Network.
    - **Key Columns**: `id`, `domain`, `path`.

2. **`wp_sitemeta`**
    
    - Analogous to `wp_options` but for the entire network.
    - Stores metadata about the network’s configuration, plugin settings applied network-wide, etc.
    - **Key Columns**: `meta_id`, `site_id`, `meta_key`, `meta_value`.

3. **`wp_blogs`**
    
    - Lists every subsite (a.k.a. “blog”) in the network.
    - **Key Columns**: `blog_id`, `site_id`, `domain`, `path`, `registered`, `last_updated`.

4. **`wp_blogmeta`** _(Introduced in WP 5.1)_
    
    - Stores metadata for each subsite (blog), similar to how `wp_sitemeta` stores network-level metadata.
    - **Key Columns**: `meta_id`, `blog_id`, `meta_key`, `meta_value`.

5. **`wp_blog_versions`**
    
    - Records the database version each subsite is on, so WordPress knows which “blogs” need database upgrades during core updates.
    - **Key Columns**: `blog_id`, `db_version`, `last_updated`.

6. **`wp_signups`**
    
    - Used if you allow new site creation via user registration.
    - Stores pending site signups that haven’t been activated yet. Once activated, entries move into `wp_blogs`.
    - **Key Columns**: `signup_id`, `domain`, `path`, `title`, `user_login`, `user_email`.

7. **`wp_registration_log`**
    
    - Logs users who create new subsites upon activation.
    - **Key Columns**: `ID`, `email`, `IP`, `blog_id`, `date_registered`.

### Updated or Global Tables

1. **`wp_users`**
    
    - Becomes a _global_ user table shared by every subsite in the network.
    - Gains extra fields, like `spam` or `deleted`, marking users’ states across the network.

2. **`wp_usermeta`**
    
    - Stores user metadata for all sites in the network.
    - For example, roles in each subsite or plugin-specific user settings.

### Duplicated Subsite Tables

For every subsite beyond the primary, WordPress generates additional sets of tables, each prefixed by the blog (subsite) ID:

- `wp_2_commentmeta`
- `wp_2_comments`
- `wp_2_links`
- `wp_2_options`
- `wp_2_postmeta`
- `wp_2_posts`
- `wp_2_terms`
- `wp_2_termmeta`
- `wp_2_term_relationships`
- `wp_2_term_taxonomy`

For subsite ID 3, you’d see `wp_3_posts`, `wp_3_options`, etc., and so on for each new subsite.

---

## Practical Implications

1. **Isolating Subsite Content**
    
    - Each subsite’s posts, comments, and taxonomies reside in its own dedicated tables. This separation helps prevent conflicts and makes it easier to manage site-specific content.

2. **Global User Base**
    
    - All network users exist in the **same** `wp_users` table. From a data perspective, a single user can have different roles on different subsites.

3. **Unified or Divergent Settings**
    
    - Network-level settings live in `wp_sitemeta`, while each subsite’s local preferences remain in their own `wp_x_options`. This structure supports a blend of shared global configurations with locally overridden values.

4. **Network Upgrades**
    
    - During WordPress updates, the system checks `wp_blog_versions` to see which subsites need a DB upgrade. This ensures each subsite’s tables remain consistent with the new WordPress version.

5. **Maintenance and Troubleshooting**
    
    - If you need to debug a problem on a specific subsite, you can focus on the relevant set of tables (e.g., `wp_5_posts`, `wp_5_options`, etc.) in the database.
    - For global issues (user logins, spam flags, etc.), you might investigate `wp_users` or `wp_usermeta`.

---

## Tips for Working with a Multisite Database

1. **Use WP-CLI**
    
    - Commands like `wp db query` or search-and-replace operations can be directed to specific subsite tables using table prefixes.
    - Example: `wp db query --prefix=wp_2_ "SELECT * FROM wp_2_posts"`

2. **Be Aware of Site IDs**
    
    - Track blog IDs (subsite IDs) in the `wp_blogs` table to know which subsite corresponds to which numbered table prefix.

3. **Database Size**
    
    - Each subsite adds another set of 10+ tables, so be mindful of how backups and migrations might grow over time.

4. **Security & Access Control**
    
    - Because all sites share users, implementing role separation and ensuring you properly manage user capabilities is crucial. A malicious user on one subsite could have ramifications across the network if roles aren’t set correctly.

5. **Backups**
    
    - Backup strategies might focus on a single database dump that encapsulates every subsite, or targeted partial backups if you only need specific subsite data. Tools often allow you to select which subsite tables to back up.

---

## Conclusion

WordPress Multisite adds essential tables (`wp_site`, `wp_sitemeta`, `wp_blogs`, etc.) for managing a network of sites and transforms certain single-site tables—**especially `wp_users`**—into global resources. Meanwhile, every subsite has its own set of site-specific tables (like `wp_2_posts`), which keep local content distinct. This architecture supports a flexible, scalable environment for organizations running multiple or multilingual sites under one WordPress installation.

Understanding these relationships is key to effectively troubleshooting, optimizing performance, and tailoring data operations across a WordPress Multisite network. When combined with the robust capabilities of plugins like **MultilingualPress**, you gain the full power of separate sites for each language, all while preserving the simplicity of a single codebase and user database.
