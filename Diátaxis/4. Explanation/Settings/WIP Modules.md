MultilingualPress offers a variety of modules that enable or extend features across your entire Multisite network. These global settings are accessible under **My Sites → Network Admin → MultilingualPress**. Each module can be activated or deactivated to tailor MultilingualPress functionality to your needs. Some settings and tabs become available only when their corresponding modules are active (e.g., Redirect, Quicklinks).

![MultilingualPress Modules Settings](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/GlobalSettings-1.png)

Below is an overview of key modules and settings:

---

## Modules Overview

- **Gutenberg Blocks**  
    Activates support for MultilingualPress Gutenberg blocks, enabling multilingual content blocks for language switchers and other features.
    
- **Alternative Language Title**  
    When enabled, adds a field on each subsite’s MultilingualPress settings page to set an alternative language title. This title appears in the Admin menu instead of the default site title.
    
- **Redirect**  
    Enables automatic language redirection.
    - Activating this module unlocks a new **Redirection** tab in global settings.
    - Provides per-site options to activate redirection and designate fallback sites for language redirects.
    - Useful for redirecting users based on language preferences when a specific language version of a page isn't available.
- **Trasher**  
    Adds a checkbox to the post editing interface. When checked, moving a post to trash sends all its translations to trash simultaneously. Useful for keeping translations in sync during deletion.
    
- **Language Manager**  
    Enables a dedicated interface to manage the available languages in the network.
    - Found under **My Sites → Network Admin → MultilingualPress → Language Manager**.
    - Allows adding custom languages or modifying existing ones, e.g. for multilingual SEO purposes.
- **Language Switcher**  
    Activates the legacy Language Switcher Widget for quick integration of a language switcher into theme-supported widget areas. Note: This legacy widget requires a non-block theme.
    
- **WooCommerce**  
    Enables WooCommerce support, including translation of products, orders, coupons, and product attributes like categories and tags.
    
- **Quicklink**  
    Renders a quick navigation link for each post translation on the front end. Additional settings allow customization of link positions.
    
- **ACF (Advanced Custom Fields)**  
    When ACF is installed and activated, this module allows MultilingualPress to manage ACF fields across translations.
    
- **Beaver Builder**  
    Enables compatibility between MultilingualPress and the Beaver Builder page builder, ensuring seamless translation of content built with Beaver.
    
- **Elementor**  
    Enables compatibility between MultilingualPress and the Elementor page builder for translating Elementor-based content.
    
- **User Information Translation Settings**  
    Allows separate translations of the “Biographical Info” field in user profiles for each language site.
    
- **Original Translation Language**  
    Adds an option when editing posts to designate content as the original language or a translation.
    
- **Comments**  
    Activates MultilingualPress support for comments across translations, enabling comment synchronization and translation.
    
- **External Sites**  
    Allows linking posts from your network to pages on external websites for language-specific content not hosted within your multisite.
    
- **MultilingualPress Site Flags**  
    Add country flags to menus, supporting visual identification of regional markets in navigation elements.
    - Offers customization for flag styles via settings or custom site flag URLs.

---

## How Global Modules Work

Each module extends MultilingualPress functionality network-wide. Enabling a module typically:

- **Adds New Features**: Makes additional options, UI elements, or compatibility layers available both globally and on individual subsite settings pages.
- **Enhances Integration**: Facilitates integration with third-party plugins (e.g., WooCommerce, ACF, Elementor, Beaver Builder), ensuring smooth multilingual operations.
- **Provides Customization**: Some modules, like the **Redirect** and **Quicklink**, introduce additional tabs or settings panels for fine-tuning behavior across the network.

---

## Tips for Using Global Modules

- **Selective Activation**: Only enable the modules you need to minimize overhead and avoid unnecessary complexity.
- **Module Dependencies**: Some modules require other plugins (e.g., ACF, WooCommerce). Ensure those plugins are installed and activated.
- **Per-Site Settings**: After activating a module globally, visit individual subsite settings to configure module-specific options (e.g., redirection behavior, alternative language titles).

---

By understanding these global modules, administrators can configure and extend MultilingualPress functionality to better suit the needs of their multilingual network. For detailed setup instructions for each module, refer to the respective **How-To** guides in the Tutorials section.