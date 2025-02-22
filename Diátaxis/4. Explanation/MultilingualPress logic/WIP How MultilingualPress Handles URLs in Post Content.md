# How MultilingualPress Handles URLs in Post Content

**Purpose**: This document clarifies how **MultilingualPress (MLP)** processes internal URLs—particularly those pointing to your Media Library—when duplicating or translating site content across subsites. While earlier versions of MLP avoided changing post content URLs, more recent releases (MLP 4.9.0+) can now automatically update certain media references in **core block editor** content, ensuring that copied images remain properly linked in the new site.

---

## Historical Context

In older MLP versions, when you copied or linked content from one language site to another, **no** internal URLs in post content were altered. This approach avoided common issues like:

- **No matching target content**: A page in the source site might not exist in the target site.
- **External vs. internal links confusion**: The plugin couldn’t reliably detect if a URL was external or local, causing broken links when external URLs were changed.
- **Performance overhead**: Parsing every URL in the post to check if it pointed to an existing remote page was resource-intensive.
- **Broken media references**: If media wasn’t duplicated, updating media URLs would lead to missing images.

---

## Modern Approach (MLP 4.9+)

### 1. **Copying Source Content with Core Blocks**

For posts and pages using the **WordPress block editor** (Gutenberg), MLP can now **replace media URLs** when you use the **“Copy source content”** option in the translation metabox. This applies to:

- **Images** in core image blocks
- **Galleries** in core gallery blocks
- **Other core block references** embedding media from your Media Library

When content is copied, MLP duplicates media attachments to the **remote site’s** Media Library (if the “Copy Attachments” option is selected). It then **updates** the URLs so that images, galleries, or file downloads point to the new site’s uploads.

> **Important**: This automatic URL rewriting only applies to **WordPress core block** references. If you use custom or third-party blocks that store media differently, MLP may not detect or change those media links.

### 2. **Classic Editor or Non-Core Content**

Content entered via:

- **Classic Editor** text fields
- **Page builders** or plugin shortcodes
- **Custom-coded references** within post content

MLP **does not** automatically rewrite URLs for these cases. The plugin can’t reliably parse arbitrary HTML or shortcodes without risking broken or external links. In such cases:

- Media may not be recognized for duplication.
- The existing media URLs will remain pointing to the source site.

### 3. **Whole Site Duplication & Media**

For **site duplication** (e.g., creating a new site “based on” an existing one):

- MLP can copy the entire Media Library to the new site if you select **“Copy attachments”**.
- For pages/posts using the **block editor**, MLP updates embedded references so images point to the newly created media objects in the duplicated site.
- Custom logic, Classic Editor HTML, or external references will remain unchanged.

---

## Why Not Replace All URLs?

Even with the improvements in media URL rewriting for block-based content, MLP still won’t alter **arbitrary** links in your content for the following reasons:

1. **Risk of Breaking External Links**
    - Rewriting URLs that might not belong to your source site is risky.
    
2. **Performance Considerations**
    - Extensive checks on HTML or other markup can slow down site duplication.
    
3. **No Guarantee of Matching Pages**
    - A URL like `example.com/en/page-slug` might not exist in `example.com/de/`. Automatically changing it to `example.com/de/page-slug` could result in a 404 if the page doesn't exist in the target language.

MLP focuses on **reliably recognized** content references, specifically **block-based media** that the plugin knows how to duplicate and link properly.

---

## Best Practices

1. **Use the Block Editor for Media**
    - If your team primarily uses the WordPress block editor for images or file embeds, MLP can easily handle media duplication.
    
2. **Check Third-Party Blocks**
    - Custom or page builder blocks may store media references differently, and MLP might not detect them. Verify if your block type is fully compatible with MLP.

3. **Manual Adjustments**
    - For Classic Editor or older content, you may need to manually edit or search-replace URLs in the target site after duplication.

4. **Validate Duplicate Sites**
    - After duplicating a site, preview key pages to ensure images and attachments display correctly.

5. **Contribute to Compatibility**
    - If you find block types or media references that MLP doesn't yet rewrite, share feedback with our support team to help improve compatibility.

---

## Conclusion

**MultilingualPress 4.9.0+** improves how media URLs are copied for core block editor content by **rewriting** them to the new site’s Media Library references upon duplication. However, links outside the standard block framework remain unchanged to prevent unintentional breakage. By using the block editor and MLP’s “Copy Attachments” feature, you can streamline multilingual content creation with minimal manual adjustments to URLs.
