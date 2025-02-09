# How to Install and Set Up a WordPress Multisite

**Purpose**: This guide helps you transform a single WordPress site into a multisite installation, covering both manual configuration steps and using the WP-CLI approach. Once enabled, you gain a **Network Admin** interface to manage multiple sites under one WordPress installation.

---

## Prerequisites

- A working **single-site** WordPress installation.
- **Pretty Permalinks** enabled (e.g., `https://example.com/my-post/` rather than `?p=123`).
- **All Plugins Disabled** before converting.
- **FTP Access** (to configure e.g. `wp-config.php` or `.htaccess` files manually).
- **WP CLI** (optional, if you want to reduce the effort to running a single command)
- **Complete Backup** of your WordPress files and database, in case you need to roll back.

---

## 1. Enable Multisite in `wp-config.php` (Manual Approach)

1. **Access Your Files**: Connect via FTP to your WordPress root directory.
2. **Edit `wp-config.php`**: Above the line `/* That's all, stop editing! Happy blogging. */`, add:
    
    ```php
    define('WP_ALLOW_MULTISITE', true);
    ```

3. **Save and Re-upload** `wp-config.php`.

> **Result**: Multisite is now enabled, but the network isn’t fully created yet.

---

## 2. Create the Multisite Network

1. **Refresh WordPress Admin**: Log back into your WordPress Dashboard.
2. **Network Setup**:
    - Navigate to **Tools → Network Setup**.
    - Choose **Subdomains** (e.g., `site1.example.com`) or **Subdirectories** (e.g., `example.com/site1`).
3. **Provide Network Details**:
    - **Network Title** (e.g., “My Multisite Network”)
    - **Admin Email** (can match your existing admin account)
4. **Install**: Click the **Install** button. WordPress will generate code snippets for `wp-config.php` and `.htaccess`.

---

## 3. Update Configuration Files

After installing the network, WordPress displays two sets of code:

1. **`wp-config.php` Snippet** (near “stop editing” line):
    
    ```php
    define('MULTISITE', true);
    define('SUBDOMAIN_INSTALL', true); // or false if subdirectories
    define('DOMAIN_CURRENT_SITE', 'example.com');
    define('PATH_CURRENT_SITE', '/');
    define('SITE_ID_CURRENT_SITE', 1);
    define('BLOG_ID_CURRENT_SITE', 1);
    ```

2. **`.htaccess` Snippet** (replaces existing WP rules):
    
    ```apache
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
    ```

3. **Save & Re-upload** both files as needed.

<!-- Note: This is the essential step to properly configure the multisite network in WordPress. A **screenshot** of the updated `wp-config.php` and `.htaccess` file can be added here to help users understand what needs to be modified. -->

---

## 4. Verify Network Admin & Settings

1. **Log Back In**: Once the files are updated, log into WordPress again.
2. **Network Admin**:
    - A new **Network Admin** menu appears in your top admin bar.
    - Manage the entire network here: create sites, oversee themes/plugins, and manage users across subsites.
3. **Network Settings**:
    - **Dashboard**: Quick links to add sites/users.
    - **Sites**: List or add subsites. Edit each site’s address, title, language, etc.
    - **Themes**: Installed once, then activated per site or network-wide.
    - **Plugins**: Similarly installed by the Super Admin, optionally activated for all sites.
    - **Settings**: Basic network defaults (e.g., new site language, user registration, etc.).

<!-- Note: This is a crucial section to help users understand what the **Network Admin** provides once activated. A **screenshot** of the Network Admin interface would greatly aid users in visualizing this new admin area. -->

---

## 5. Adding New Sites

1. Go to **My Sites → Network Admin → Sites**.
2. Click **Add New** to create a subsite.
3. Specify:
    - **Site Address** (`site1.example.com` or `example.com/site1`).
    - **Site Title** (e.g., “Blog A”).
    - **Site Language** (default locale for the subsite admin).
    - **Admin Email** (assign an existing user or create a new admin).

<!-- Note: This is the step where users can add new subsites. Including a **screenshot** of the "Add New Site" form would help visualize the fields needed. -->

---

## 6. Converting to Multisite via WP-CLI (Alternative Approach)

If you prefer using **WP-CLI**:

1. **Install WP-CLI** (if not available):
    
    ```bash
    curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
    chmod +x wp-cli.phar
    sudo mv wp-cli.phar /usr/local/bin/wp
    wp --info
    ```

2. **Navigate to WP Root**:
    
    ```bash
    cd /var/www/html/your-site
    ```

3. **Backup** your site and database.
4. **Convert** to multisite:
    
    ```bash
    wp core multisite-convert
    ```

5. **Update Config**: WP-CLI will provide instructions similar to the manual method for `wp-config.php` and `.htaccess`.
6. **Remove “/blog/” Prefix (Optional)**:
    - If your primary site’s URLs show a “/blog/” slug, remove it by resetting the permalink structure:
        
        ```bash
        wp option update permalink_structure "/%postname%/"
        wp rewrite flush
        ```

7. **Tip**: For a **multilingual** network, **MultilingualPress** offers additional CLI commands to automate content links, attachments, and bulk site creation—saving time when adding new languages or replicating site structures.

<!-- Note: This section offers an alternative method for those familiar with WP-CLI. A **screenshot** showing how WP-CLI commands are entered in the terminal would be useful for users unfamiliar with the command line. -->

---

## 7. Managing Themes, Plugins, and Users

- **Themes**: Only a Super Admin can install or remove them. Local admins can activate themes on their sites if allowed in **Network Settings**.
- **Plugins**: Similarly installed at the network level. Site admins typically only activate/deactivate them locally.
- **Users**: A single user table is shared across the network. Assign roles on each subsite. One user could be an Editor on Site A, an Admin on Site B.

<!-- Note: Users should be aware of the limitations around theme and plugin management. A **screenshot** of the Network Admin user and plugin sections would be beneficial to visualize roles and activations. -->

---

## Conclusion

WordPress Multisite can be set up either manually—by editing `wp-config.php`, `.htaccess`, and the network setup screen—or via a single WP-CLI command (`wp core multisite-convert`). Once active, a **Network Admin** interface centralizes theme/plugin installations, user management, and site creation.

This architecture is ideal for **multiple sites**, including **multilingual** networks, because each subsite remains autonomous yet benefits from unified updates. Explore more scenarios in [WordPress Multisite for Different Scenarios](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d?model=o1#) to understand how organizations, universities, and global brands leverage multisite for efficient site management.

<!-- Note: A **final screenshot** showing the Multisite network setup in action or the final configuration step would help wrap up the guide effectively. -->
