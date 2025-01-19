**Purpose**: This document explains _why_ using **WordPress Multisite** plus **MultilingualPress** is an optimal way to create a **multilingual WooCommerce** shop, highlights key features and limitations, and provides an overview of the setup process.

---

## Why MultilingualPress + WooCommerce?

1. **Independent Language Sites**
    
    - Each language resides on its own subsite—ensuring faster load times and fewer conflicts than single-site solutions that pile multiple languages into one database.
    - The subsite approach also allows you to configure WooCommerce settings (e.g., shipping, taxes, currency) differently per language or region.
2. **Clean Architecture & No Lock-In**
    
    - MultilingualPress relies on the native **WordPress Multisite** feature. If you uninstall MultilingualPress, each site remains intact and fully operational—no shortcodes or custom fields left behind.
3. **Flexible Design & Functionality**
    
    - Adapt each language’s site to local expectations. For instance, you might add region-specific plugins (like a German legal compliance plugin) only to the German shop, without affecting other sites.
4. **Performance & Scalability**
    
    - Large eCommerce stores handle substantial traffic. By isolating each language to its own subsite, you keep overhead smaller and deliver faster page loads compared to single-site multilingual alternatives.
5. **Tight Control Over Plugins & Themes**
    
    - Only the **Super Admin** can install network-wide plugins and themes, ensuring consistent brand identity and fewer accidental conflicts.

---

## Setting Up a Multilingual WooCommerce Shop (High-Level Overview)

1. **Enable WordPress Multisite**
    
    - Either install WordPress as multisite from the start or [convert an existing single-site to multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/).
2. **Install WooCommerce**
    
    - Choose whether you _network activate_ WooCommerce (applies to all sites automatically) or activate it on individual subsites to configure unique shipping, payment gateways, or currency per language site.
3. **Install MultilingualPress**
    
    - Network Activate **MultilingualPress**, giving each subsite tools to link products, pages, and posts across languages.
4. **Create a Subsite per Language**
    
    - For example, create an English subsite, a French subsite, a Spanish subsite, etc.
    - Assign each site a distinct domain or subfolder (e.g. `store.fr.example.com` or `example.com/fr`). Use [domain mapping](https://multilingualpress.org/docs/domain-mapping) for region-specific top-level domains if desired.
5. **Link Products & Pages Across Languages**
    
    - Edit a product in the main language site; use the **translation metaboxes** below the editor to link or copy that product to the other language sites.
    - Repeat for relevant pages (e.g., “Cart,” “Checkout”).
6. **Decide on Stock Management**
    
    - By default, each subsite has its own inventory. If you want a **shared stock**, consider [Central Stock for WooCommerce](https://wp-centralstock.com/) which synchronizes product inventory across the multisite network.
7. **Customize Each Store**
    
    - Adjust shipping zones, taxes, or payment gateways in **WooCommerce** on each language subsite. Some regions may need special shipping carriers, or a different currency.
    - Use .po/.mo files or a translation plugin (e.g. Loco Translate) to localize WooCommerce system strings (like email templates).
8. **Language Switching for Customers**
    
    - MultilingualPress provides optional **automatic redirection** to match visitors’ browser language.
    - You can also place a **language switcher** in menus or widget areas, allowing customers to hop between language versions of the same product.

---

## Current Limitations & Workarounds

1. **Shopping Cart Sync**
    
    - Carts are not synchronized across languages out of the box. If a customer adds items in the English shop, those items won’t appear in the French site’s cart.
    - **Tip**: Usually accepted as normal because each subsite is truly independent, often with unique currency or shipping rules.
2. **User Sync**
    
    - By default, all subsites share the same `wp_users` table, so accounts are recognized network-wide. However, roles can differ per subsite.
    - If you need full user data sync across subsites (e.g., single sign-on or membership logic), you can further configure or rely on network-level plugins.
3. **Custom Fields & Plugin Data**
    
    - MultilingualPress doesn’t automatically transfer all WooCommerce-specific meta fields (like prices in multiple currencies) unless you manually configure or rely on advanced features.
    - You can, however, create localized variants of a product on each subsite and update pricing manually.
4. **Translation of System Messages**
    
    - Certain emails or front-end strings may require separate translation. Tools like Loco Translate can help localize the entire WooCommerce interface.

---

## Example Workflow

1. **Main Store Setup**: Start with the English store. Configure currency, shipping, and product settings. Add initial products.
2. **Create a French Subsite**: Use MultilingualPress’s **Based on Site** option to copy settings and content from the English store.
3. **Activate/Adjust**: On the French subsite, refine shipping, currency, and tax rules. Translate product names, descriptions, or variations.
4. **Add a Language Switcher**: Provide a link or widget that connects “Product X” in English to “Produit X” in French.
5. **Check Inventory**: If each site’s stock is separate, maintain them individually. For shared inventory, use [Central Stock for WooCommerce](https://wp-centralstock.com/) (or a similar solution).
6. **Continue Expanding**: Add more language subsites as your market grows (Spanish, German, etc.), each with its own local configuration.

---

## Key Advantages for Multilingual E-Commerce

- **High Performance**: Each subsite loads only its language resources, not an entire multi-language overhead.
- **SEO Benefits**: Each language site can have localized domain structures and optimized metadata, improving search rankings for region-specific queries.
- **No Plugin Lock-In**: If you remove MultilingualPress, each store remains a fully functional site with no leftover shortcodes or content lock issues.

---

## Conclusion

Combining **WordPress Multisite**, **WooCommerce**, and **MultilingualPress** provides a **scalable, flexible**, and **future-proof** solution for building a multilingual online store. Each language site can have unique WooCommerce settings, produce optimal performance, and maintain a clean separation of content—while still connecting products across languages in a user-friendly manner.

- **Start** by [installing a Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/) and adding [MultilingualPress](https://multilingualpress.org/).
- **Configure** each WooCommerce subsite (language) with distinct shipping, taxes, and currency rules.
- **Translate** or link product content using the intuitive metaboxes, optionally customizing each store’s design or plugin set.

This approach lets you serve global customers in their preferred language, all while ensuring robust performance and streamlined management from a single WordPress installation.