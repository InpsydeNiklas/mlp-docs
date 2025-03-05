## Can I use MultilingualPress with a regular single WordPress site?

### **Multisite Is Required for MultilingualPress**

**Short Answer**  
MultilingualPress cannot run on a standard single-site WordPress installation. You must have a WordPress multisite network to take advantage of its features.

### **Why Do I Need a Multisite Setup?**

MultilingualPress is designed to create a dedicated site for each language. This means that when someone visits your English site, they are actually visiting a distinct site within your multisite network—separate from, say, your French site. By using discrete sites, all translated content remains clean and unaltered, which makes it easy to manage and avoids potential content loss, e.g., if the plugin is deactivated.

**Single-Site Multilingual Plugins** vs **MultilingualPress**:

- Single-site multilingual plugins often need to alter how WordPress saves content—typically through injected shortcodes, custom fields, or custom post structures. These plugins can introduce dependencies on shortcodes or other mechanisms that are tightly bound to the site’s architecture.
- When these plugins are deactivated, the translations may become inaccessible or break, leading to potential issues with content consistency.
- **MultilingualPress**, however, stores translation links in its own database tables, completely separating the content for each language site. This means:
    - Translations remain unaffected by plugin deactivation.
    - Each site operates independently, preserving the integrity of your content, which can be fully backed up or migrated without any dependency on the plugin.

### **What If I Only Have a Single-Site Installation Right Now?**

If you’re currently running a single-site WordPress installation, you can easily switch it to a multisite network. Here's why this is a good idea:

- **Full Control Over Language Sites**: You gain independent control over each language’s settings, users, and content while keeping them interconnected for translations.
- **Scalability**: As your content needs grow, it's easier to scale your multilingual website using WordPress Multisite, especially with MultilingualPress.
- **Custom Solutions**: Each language can have its own tailored functionality, like custom plugins, themes, and even specific compliance regulations (e.g., legal disclaimers for different regions).

**Follow the detailed instructions in** [How to Install WordPress Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/) **to convert your setup and unlock MultilingualPress’s full functionality.**

For additional resources on setting up WordPress Multisite, check out the following:

- **[Setting up a WordPress multisite network](https://learn.wordpress.org/lesson/setting-up-a-wordpress-multisite-network/)**
- **[Managing a WordPress multisite network](https://learn.wordpress.org/lesson/managing-a-wordpress-multisite-network/)**

---

### **Next Steps**

1. **Configure Your Multisite**:  
    Once you have a WordPress multisite in place, make sure you set it up properly by following the guide mentioned above. This ensures the multisite environment is optimized for use with MultilingualPress.
    
2. **Install MultilingualPress**:  
    After setting up your multisite network, proceed to follow our [step-by-step guide](#) to install and activate MultilingualPress.
    

---

### **Benefits of Transitioning to Multisite for Multilingual Websites**

Here’s why switching to WordPress Multisite with MultilingualPress is a great idea:

1. **Better Content Management**:  
    Each language has its own independent site with content that’s easier to manage, making it simple to update, backup, and scale.
2. **Consistent Branding**:  
    Maintain a consistent brand identity across multiple regions while delivering localized content for each audience.
3. **Enhanced SEO**:  
    MultilingualPress automatically handles SEO aspects like hreflang tags, and keeping each language as a separate site helps with SEO clarity.
4. **Improved Performance**:  
    Multisite setups allow for more efficient resource usage, minimizing issues related to performance and uptime, even when handling multiple language versions of your site.

---

### **Conclusion**

By switching to a multisite network, you can ensure your multilingual content is always secure, portable, and easy to manage—even after deactivating or removing MultilingualPress. With MultilingualPress, you’re equipped to scale globally, keeping your translations consistent and ensuring your multilingual website grows smoothly as your audience expands.