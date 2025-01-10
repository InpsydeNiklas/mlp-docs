## Multisite Is Required for MultilingualPress

**Short Answer**  
MultilingualPress cannot run on a standard single-site WordPress installation. You must have a WordPress multisite network to take advantage of its features.

**Why Do I Need a Multisite Setup?**  
MultilingualPress is designed to create a dedicated site for each language. This means that when someone visits your English site, they are actually visiting a distinct site within your multisite network - separate from, say, your French site. By using discrete sites, all translated content remains clean and unaltered, which makes it easy to manage and avoids potential content loss, e.g. if the plugin is deactivated.

Single-site multilingual plugins often need to alter how WordPress saves content -typically through injected shortcodes or other custom structures. Once those plugins are deactivated, your translations can become inaccessible, effectively breaking your site(s). Because MultilingualPress stores translation links in its own tables, each language site remains independent and “shortcode-free”. This not only keeps your content portable and intact but also aligns with WordPress best practices.

**What If I Only Have a Single-Site Installation Right Now?**  
If you’re currently running a single-site WordPress installation, you can switch it to a multisite network. Follow the detailed instructions in [How to Install WordPress Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/) to convert your setup and unlock MultilingualPress’s full functionality.

Additional details can be found in this introduction to WordPress multisite course:
## [Setting up a WordPress multisite network](https://learn.wordpress.org/lesson/setting-up-a-wordpress-multisite-network/)

## [Managing a WordPress multisite network](https://learn.wordpress.org/lesson/managing-a-wordpress-multisite-network/)

---

### Next Steps

- **Configure Your Multisite**: Once you have a WordPress multisite in place, learn how to set it up properly.
- **Install MultilingualPress**: Next, follow our step-by-step guide to install and activate MultilingualPress.

By using a multisite network, you ensure your multilingual content is always secure, portable, and easy to manage - even after deactivating or removing MultilingualPress.