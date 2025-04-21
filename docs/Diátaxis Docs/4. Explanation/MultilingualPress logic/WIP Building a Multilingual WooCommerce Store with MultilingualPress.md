# Building a Multilingual WooCommerce Store with MultilingualPress

**Purpose**: This document explains why using **WordPress Multisite** combined with **MultilingualPress** is an optimal solution for creating a **multilingual WooCommerce** store. It highlights the key features, addresses common limitations, and provides a comprehensive overview of the setup process.

---

## Why Choose MultilingualPress + WooCommerce?

### 1. **Independent Language Sites**
   - **Separate Language Subsites**: Each language resides on its own subsite, offering faster load times and fewer conflicts than single-site solutions. This method avoids the complexity of managing multiple languages within one database.
   - **Customizable WooCommerce Settings**: You can configure WooCommerce settings (such as shipping, taxes, and currency) differently per language or region, making it easier to handle local requirements.

### 2. **Clean Architecture & No Lock-In**
   - MultilingualPress relies on the native **WordPress Multisite** feature. If you uninstall MultilingualPress, each language subsite remains intact and fully operational. No shortcodes or custom fields are left behind, ensuring a clean removal process.

### 3. **Flexible Design & Functionality**
   - **Localization Flexibility**: Each language’s site can be adapted to local expectations. For example, you can add region-specific plugins (like a legal compliance plugin for Germany) without affecting other sites in the network.

### 4. **Performance & Scalability**
   - By isolating each language to its own subsite, you ensure better performance and scalability. This architecture allows for faster page loads compared to single-site multilingual solutions, and it can scale better to handle large amounts of traffic.

### 5. **Tight Control Over Plugins & Themes**
   - Only the **Super Admin** can install network-wide plugins and themes, ensuring consistent brand identity and fewer accidental conflicts. This level of control minimizes risks associated with plugins or themes added by individual users.

---

## Setting Up a Multilingual WooCommerce Shop (High-Level Overview)

### 1. **Enable WordPress Multisite**
   - Either install WordPress as multisite from the start or [convert an existing single-site to multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/).

### 2. **Install WooCommerce**
   - Decide whether to **network activate** WooCommerce (applies to all sites automatically) or activate it on individual subsites to configure unique shipping, payment gateways, or currency per language site.

### 3. **Install MultilingualPress**
   - **Network Activate** MultilingualPress, providing each subsite with the tools needed to link products, pages, and posts across languages.

### 4. **Create a Subsite per Language**
   - For example, create an English subsite, a French subsite, a Spanish subsite, etc.
   - Assign each site a distinct domain or subfolder (e.g. `store.fr.example.com` or `example.com/fr`). Use [domain mapping](https://multilingualpress.org/docs/domain-mapping) for region-specific top-level domains if desired.

### 5. **Link Products & Pages Across Languages**
   - Edit a product on the main language site and use the **translation metaboxes** below the editor to link or copy that product to the other language sites.
   - Repeat the process for other relevant pages (e.g., “Cart,” “Checkout”).

### 6. **Decide on Stock Management**
   - By default, each subsite has its own inventory. If you want **shared stock**, consider [Central Stock for WooCommerce](https://wp-centralstock.com/) to synchronize product inventory across the multisite network.

### 7. **Customize Each Store**
   - Adjust shipping zones, taxes, and payment gateways in **WooCommerce** for each language subsite. Some regions may require different shipping carriers or currency options.
   - Use .po/.mo files or a translation plugin (e.g., Loco Translate) to localize WooCommerce system strings, such as email templates.

### 8. **Language Switching for Customers**
   - MultilingualPress offers optional **automatic redirection** to match visitors' browser language.
   - Alternatively, place a **language switcher** in menus or widget areas, allowing customers to easily switch between different language versions of the same product.

---

## Current Limitations & Workarounds

### 1. **Shopping Cart Sync**
   - Carts are not synchronized across languages by default. Items added in the English shop won't appear in the French site’s cart.
   - **Tip**: This is generally accepted as normal since each subsite is independent, with unique shipping and currency settings.

### 2. **User Sync**
   - All subsites share the same `wp_users` table, so accounts are recognized network-wide. However, roles can differ per subsite.
   - For full user data synchronization (e.g., single sign-on or membership logic), consider network-level plugins or further configuration.

### 3. **Custom Fields & Plugin Data**
   - MultilingualPress doesn’t automatically transfer all WooCommerce-specific meta fields (like prices in multiple currencies) unless manually configured or with advanced features.
   - Consider creating localized variants of products on each subsite and manually updating pricing.

### 4. **Translation of System Messages**
   - Some system messages, such as emails or front-end strings, may require separate translation.
   - Tools like **Loco Translate** can help localize the entire WooCommerce interface.

---

## Example Workflow

### 1. **Main Store Setup**
   - Start with the English store. Configure currency, shipping, and product settings. Add initial products.

### 2. **Create a French Subsite**
   - Use MultilingualPress’s **Based on Site** option to copy settings and content from the English store.

### 3. **Activate/Adjust**
   - On the French subsite, refine shipping, currency, and tax rules. Translate product names, descriptions, or variations.

### 4. **Add a Language Switcher**
   - Provide a link or widget that connects the English product ("Product X") to the French product ("Produit X").

### 5. **Check Inventory**
   - If stock is separate, maintain inventory individually for each subsite. For shared inventory, use [Central Stock for WooCommerce](https://wp-centralstock.com/).

### 6. **Continue Expanding**
   - Add more language subsites as your market grows (Spanish, German, etc.), each with its own local configuration.

---

## Key Advantages for Multilingual E-Commerce

- **High Performance**: Each subsite loads only its language resources, reducing multi-language overhead and improving load times.
- **SEO Benefits**: Each language site can have localized domain structures and optimized metadata, improving search rankings for region-specific queries.
- **No Plugin Lock-In**: If you remove MultilingualPress, each store remains a fully functional site with no leftover shortcodes or content lock issues.

---

## Conclusion

Combining **WordPress Multisite**, **WooCommerce**, and **MultilingualPress** provides a **scalable, flexible**, and **future-proof** solution for building a multilingual online store. Each language site can have unique WooCommerce settings, ensuring optimal performance, and maintaining clean separation of content, all while connecting products across languages in a user-friendly manner.

- **Start** by [installing a Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/) and adding [MultilingualPress](https://multilingualpress.org/).
- **Configure** each WooCommerce subsite (language) with distinct shipping, taxes, and currency rules.
- **Translate** or link product content using the intuitive metaboxes, and optionally customize each store’s design or plugin set.

This approach lets you serve global customers in their preferred language while ensuring robust performance and streamlined management from a single WordPress installation.
