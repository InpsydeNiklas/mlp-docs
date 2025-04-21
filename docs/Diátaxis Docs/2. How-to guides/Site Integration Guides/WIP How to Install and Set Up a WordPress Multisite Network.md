**Purpose**: This comprehensive guide walks you through transforming a single WordPress site into a fully functional Multisite network. It covers preparation, enabling Multisite, configuration steps, and key considerations, combining manual and WP-CLI approaches for clarity.

---

## Prerequisites

- A working **single-site** WordPress installation.
- **Pretty Permalinks** enabled (e.g., `https://example.com/my-post/`).
- All active plugins **deactivated**.
- FTP or SSH access to your server (if performing manual steps).
- A **complete backup** of your WordPress files and database.

---

## Step 0: Before You Begin

Before starting:

- **Plan Your Network Structure**: Decide if you want **subdomains** (e.g., `site1.example.com`) or **subdirectories** (e.g., `example.com/site1`). This choice affects DNS and rewrite rules.
- **Backup**: Ensure you have backups for safety.
- **Test Environment**: Consider testing on a staging server if possible.
- **Read Official Guidance**: Familiarize yourself with [Create A Network](https://developer.wordpress.org/advanced-administration/multisite/create-network/) for deeper planning insights.

---

## Step 1: Prepare Your WordPress Installation

1. **Backup Your Site**: Save copies of your files and database.
2. **Verify Permalinks**: Ensure custom permalinks are working (`Settings → Permalinks`).
3. **Deactivate Plugins**: Disable all active plugins temporarily to prevent conflicts during setup.

---

## Step 2: Enable Multisite Feature

1. **Edit wp-config.php**:
    - Connect via FTP/SSH to your WordPress root directory.
    - Open `wp-config.php` and add:
        
        ```php
        define('WP_ALLOW_MULTISITE', true);
        ```
        
        Place this line above `/* That's all, stop editing! Happy blogging. */`.
    - Save and re-upload the file.
2. **Refresh Dashboard**: Log back into WordPress. You should now see a **Network Setup** option under **Tools**.

---

## Step 3: Create the Multisite Network

1. **Access Network Setup**:
    - Navigate to **Tools → Network Setup** in your WordPress admin.
2. **Choose Structure**:
    - Decide between **Subdomains** and **Subdirectories** based on your planned network.
    - Note: Wildcard DNS may be needed for subdomain installations.
3. **Enter Network Details**:
    - Fill in **Network Title** and **Admin Email**.
    - Review the provided information and click **Install**.
4. **Follow Prompts**:
    - WordPress displays code snippets for updating `wp-config.php` and `.htaccess`. Prepare to copy these in the next step.

---

## Step 4: Enable the Network

1. **Update Configuration Files**:
    - Add the provided lines to your `wp-config.php` (near where you added `WP_ALLOW_MULTISITE`).
    - Replace your existing WordPress rules in `.htaccess` with the new snippet.
    - Save changes and upload the files.
2. **Re-login**: Log out and log back in to see the new **Network Admin** menu in the admin bar.
3. **Remove “/blog/” Prefix (if applicable)**:
    - On subfolder installations, the main site URLs may include `/blog/`. To remove it, update permalinks or use WP-CLI:
        
        ```bash
        wp option update permalink_structure "/%postname%/"
        wp rewrite flush
        ```
        

**Tip**: If you prefer a faster setup or wish to script the process, consider using WP-CLI commands as discussed in our [WP-CLI Multisite Setup Tip](#).

---

## Step 5: Explore Network Admin & Settings

1. **Network Admin Dashboard**:
    - Access via **My Sites → Network Admin**.
    - Manage all sites, plugins, themes, and users from here.
2. **Key Sections**:
    - **Dashboard**: Overview, quick site/user addition.
    - **Sites**: List of all subsites, with options to edit or add new ones.
    - **Themes/Plugins**: Install and activate resources network-wide or per site.
    - **Settings**: Configure network defaults, such as registration settings, default language, and theme/plugin menus for site admins.

---

## Step 6: Advanced Considerations

- **Domain Mapping**: After setting up your multisite, use domain mapping (native in WordPress 4.5+) to assign custom domains to subsites. Refer to our [Domain Mapping guide](https://developer.wordpress.org/advanced-administration/multisite/domain-mapping/) for detailed steps.
- **Permalink Issues**: If you encounter permalink problems, revisit **Settings → Permalinks** and save changes to flush rewrite rules.
- **File Permissions**: Verify the `wp-content/uploads` directory is writable (permissions 755).
- **User Roles & Capabilities**: Understand that site admins have limited capabilities compared to Super Admin. Additional plugins or settings can modify these permissions if needed.
- **Plugin & Theme Management**:
    - Only Super Admin can install/upgrade plugins and themes.
    - Site admins can activate or deactivate available options if allowed in **Network Settings**.

---

## Conclusion

By following these steps, you’ll successfully convert a single WordPress installation into a robust Multisite network. This setup provides a centralized administration dashboard for managing multiple sites—including multilingual ones with **MultilingualPress**—efficiently and at scale. For more detailed scenarios, troubleshooting advanced settings, or exploring integration with MultilingualPress, refer to our extended documentation and guides.

---

**Next Steps**:

- [How to Install MultilingualPress](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)
- [WordPress Multisite for Different Scenarios](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)
- [Domain Mapping in WordPress Multisite](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)