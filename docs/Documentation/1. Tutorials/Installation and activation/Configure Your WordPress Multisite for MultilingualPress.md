---
title: Configure Your WordPress Multisite for MultilingualPress
nav_order: 2
parent: Tutorials
has_children: false
---
# Configure Your WordPress Multisite for MultilingualPress

**Purpose:** Ensure users have a proper WordPress Multisite environment before installing MultilingualPress.

---

### 1. Check Basic Requirements

- **WordPress Version:** 6.5 or higher  
- **PHP Version:** 8.0 or higher  
- **Multisite Server Requirements:** Refer to the official [Multisite server requirements](https://developer.wordpress.org/advanced-administration/multisite/prepare-network/#server-requirements).

> **Note:** MultilingualPress **cannot** run on a single-site WordPress installation.  
> Learn more: [Can I use MultilingualPress with a regular single WordPress site?](#)

---

### 2. Understand WordPress Multisite

If you’re new to multisite, check out this overview: [What is WordPress Multisite?](https://learn.wordpress.org/lesson/what-is-wordpress-multisite/).  
If you already have a multisite network set up, skip ahead to [Install MultilingualPress](#).

---

### 3. Set Up Your WordPress Multisite Network

#### **Enable Multisite in WordPress**

1. Open your `wp-config.php` file.  
2. Add the following line **above** the line that says `/* That's all, stop editing! Happy publishing. */`:
   
   ```php
   define('WP_ALLOW_MULTISITE', true);
   ```

3. Save the file and refresh your WordPress dashboard.  
4. Go to **Tools > Network Setup** to configure your multisite network.

#### **Configure `.htaccess` and `wp-config.php`**

After enabling multisite, WordPress will provide custom rules for `.htaccess` and `wp-config.php`. Follow those instructions carefully.

For detailed steps, refer to:
- [Setting Up a WordPress Multisite Network](https://learn.wordpress.org/lesson/setting-up-a-wordpress-multisite-network/)  
- [Create a Network](https://developer.wordpress.org/advanced-administration/multisite/create-network/)

> **Tip:** Consider using WP-CLI for faster setup: [Setting up Multisite with WP-CLI](#)

---

### 4. Troubleshooting Common Multisite Issues

- **Permalink Issues:** If custom permalinks don’t work, reset your permalink settings in **Settings > Permalinks**.
- **File Upload Errors:** Ensure the `wp-content/uploads` folder has the correct permissions (`755`).
- **Subdomain Not Working:** Check DNS settings and wildcard subdomain configuration.

---

### 5. Next Steps

Once your multisite network is running smoothly, proceed to [Install MultilingualPress](#) to enable multilingual capabilities.

By confirming hosting requirements and creating a proper multisite network, you lay the foundation for a seamless multilingual experience with MultilingualPress.

