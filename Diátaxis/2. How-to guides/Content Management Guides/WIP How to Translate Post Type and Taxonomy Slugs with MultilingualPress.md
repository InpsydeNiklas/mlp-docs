**Purpose**: Help you set or change localized slugs for your custom post types and taxonomies on each site, ensuring that language switchers, hreflang attributes, and other links display correctly.

---

## 1. Provide a Translated Slug During Registration

1. **Register Your CPT/Taxonomy**
    
    - Use [register_post_type](https://developer.wordpress.org/reference/functions/register_post_type/) or [register_taxonomy](https://developer.wordpress.org/reference/functions/register_taxonomy/) with the `rewrite` parameter.
    - Example:
        
        ```php
        register_post_type('my_cpt', [
          'label'   => __('My Custom Post', 'textdomain'),
          'public'  => true,
          'rewrite' => ['slug' => esc_html__('my-cpt', 'textdomain')],
        ]);
        ```
        
    - In a multisite, register the CPT/Taxonomy **per site** or in a network-wide plugin, ensuring you provide localized slug values for each language site.
2. **Alternatively, Use a Plugin (e.g., CPT UI)**
    
    - In [CPT UI](https://wordpress.org/plugins/custom-post-type-ui/) or similar plugins, look for “Custom Rewrite Slug” and **enter the translated slug** per site.

> **Result**: If each site’s registration code (or plugin setting) uses a localized slug, **MultilingualPress** automatically detects and uses it for language switchers and hreflang URLs.

---

## 2. Translate Slugs After Registration (Using Permalinks Settings)

If you did **not** specify a custom rewrite slug at registration, you can still translate slugs from the **Post Type Slugs** menu in MultilingualPress:

1. **Enable Translatable Post Types**
    
    - In Network Admin, go to **My Sites → Network Admin → MultilingualPress → Settings**.
    - Under **Translatable Post Types**, ensure the desired CPT or taxonomy is checked. Otherwise, it will appear “greyed out.”
2. **Open the Permalinks Settings**
    
    - For each language site, go to **Settings → Permalinks** in that site’s Dashboard.
    - Scroll to **Post Type Slugs** (MultilingualPress automatically adds this section).
3. **Enter a Translated Slug**
    
    - Type the localized slug you want in the field for your CPT or taxonomy.
    - Example: Instead of “my-cpt,” you might use “mon-cpt” (French) or “mein-cpt” (German).
4. **Save Permalinks**
    
    - Click **Save Changes** to flush the rewrite rules.
    - This ensures the new slug is applied site-wide.

> **Note**: Changing slugs affects existing URLs, so be prepared to regenerate permalinks or set up redirects if you already have published content.

---

## 3. Verify the Changes

1. **Visit the Front End**
    - Navigate to a custom post type archive or single post.
    - Confirm the URL now displays the localized slug (e.g., `/de/mein-cpt/post-name/`).
2. **Test Language Switcher**
    - If you have a **language switcher** (menu or widget), switch between language sites to confirm the correct translated slug appears in the URL.
3. **Check hreflang**
    - If using hreflang tags, confirm they reflect the updated slug for each locale.

---

## 4. Troubleshooting

- **Slug Field is Greyed Out**
    - Ensure your CPT is **checked** in **MultilingualPress → Settings → Translatable Post Types**.
- **Permalinks Not Updating**
    - Try re-saving permalinks again or temporarily disabling caching plugins.
- **Language Switcher Links Not Reflecting New Slug**
    - Double-check that you updated **all** relevant sites. Each language site must have its own localized slug.

---

## Summary

- **Best Practice**: Provide localized slugs directly in the `rewrite` parameter during CPT/Taxonomy registration, or via CPT UI’s “Custom Rewrite Slug.”
- **After Registration**: If no slug was set initially, use **Settings → Permalinks** on each site to fill in the translated slug fields.
- **Flush Permalinks**: Always save permalinks after changing slugs to ensure updates take effect.

By following these steps, you’ll ensure each language site in your multisite network has a **properly localized** slug for your custom post types and taxonomies—giving visitors and search engines a clear, language-specific URL structure.