# SEO Meta Sync in MultilingualPress

**Purpose**: This explanation highlights the **SEO meta sync** module available in **MultilingualPress 4.9+**, which streamlines the process of linking and managing SEO metadata across multiple language sites in a WordPress Multisite network—especially when using popular SEO plugins like Yoast or Rank Math. For older versions of MultilingualPress (pre-4.9.0), a separate add-on was required. This document clarifies how the integrated module works, why it’s beneficial, and what to do if you’re still on an older MultilingualPress release.

---

## What Is SEO Meta Sync in MultilingualPress?

- **Unified SEO Editing**: The SEO meta sync feature extends each SEO plugin’s meta boxes (e.g., Yoast, Rank Math) to other languages in your editor. Instead of switching between sites to manage SEO for each translation, you can adjust metadata for all language versions in one place.
- **Supported Plugins**: While originally designed for Yoast SEO, this integration was expanded to accommodate other popular SEO plugins, ensuring broader compatibility.
- **Where It Lives**: Since **MultilingualPress 4.9.0**, the SEO meta sync functionality is built directly into the core plugin—no separate add-on is necessary.

### Key Benefits

- **Efficiency**: Edit SEO titles, meta descriptions, focus keywords, and other plugin-specific fields for each language site from a single edit screen.
- **Fewer Redirects**: Eliminates the need to open every site’s dashboard when updating SEO metadata, saving time for authors and site managers.
- **Broad Compatibility**: Supports major SEO plugins; if your SEO tool integrates seamlessly with single-site WordPress, it’s likely to be recognized by the SEO meta sync module in MultilingualPress.

---

## Using SEO Meta Sync (MLP 4.9+)

1. **Network Environment**
    
    - Ensure you’re running **WordPress Multisite** and **MultilingualPress 4.9 or newer**.
    - Install and network-activate your chosen SEO plugin (e.g., **Yoast SEO**, **Rank Math**) or activate it only on the subsites where it’s needed.
2. **Enable SEO Meta Sync**
    
    - In your **Network Admin**, navigate to **MultilingualPress → Modules**.
    - Check the box for **“SEO Meta Sync”** (or similarly named setting) to ensure the module is active across your network.
3. **Edit Content**
    
    - Edit a post or product on your primary language site. Scroll down to the familiar SEO meta box (Yoast, Rank Math, etc.).
    - You’ll see **additional tabs** or sections for each connected language.
    - Add or modify metadata, such as focus keywords and meta descriptions, for each language version right there—no need to switch subsites.
4. **Save & Verify**
    
    - Click **Update**.
    - MultilingualPress pushes the relevant SEO fields to the corresponding language sites, ensuring consistent metadata across the network.
    - Optionally, check the translated sites’ SEO plugin meta boxes if you want to confirm the sync was successful.

<!-- Note: A **screenshot** is needed here to show the **SEO Meta Sync** interface in the editor, particularly the **additional tabs** that appear for each language. This will help readers visually understand where to find the metadata fields for each language. -->

---

## Older Versions of MultilingualPress (Before 4.9.0)

- **Separate Add-On**: If you’re on **MLP < 4.9**, a standalone plugin called **MultilingualPress-Yoast-SEO-Sync** once provided this integration.
- **Compatibility**: It was limited to Yoast and wasn’t officially tested with other SEO plugins.
- **Recommendation**: Update to **MultilingualPress 4.9.0+** to benefit from the built-in SEO meta sync module and broader SEO plugin support.

---

## FAQs & Tips

1. **Which SEO Fields Can Be Synced?**
    
    - Typically, post-level fields like **SEO title**, **meta description**, and **focus keyword**. Some plugins may store social previews or advanced analytics fields which do not interact with MultilingualPress.
2. **Partial Sync**
    
    - Copy either all, or just certain fields, you control which fields to adjust into MultilingualPress’s synchronization filters or disabling certain fields in the SEO plugin.
3. **Troubleshooting**
    
    - Ensure both the SEO plugin and MultilingualPress modules are active on each subsite.
    - Flush caches or check plugin conflict if metadata doesn’t appear in a target language.
    - Confirm that you have the correct translation relationships set up between sites.
4. **Enterprise Scenarios**
    
    - For large networks, the SEO meta sync can dramatically reduce overhead—centralizing SEO management for dozens or hundreds of language sites.

<!-- Note: A **screenshot** or **image** here could demonstrate how to enable the **SEO Meta Sync** feature in **MultilingualPress → Modules**, showing users exactly where to find this setting in their dashboard. -->

---

## Conclusion

With **MultilingualPress 4.9+**, **SEO Meta Sync** is baked right into the plugin—**no add-on required**—to streamline and unify your SEO editing process across multiple language sites. It supports key fields from major SEO plugins like Yoast and Rank Math, letting you handle multilingual SEO from one screen. If you’re still on older MultilingualPress versions, consider upgrading to harness these expanded capabilities.

<!-- Note: A **final screenshot** of the SEO fields syncing across languages in the editor would help summarize the process and provide a comprehensive visual of how this feature works in practice. -->
