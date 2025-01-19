**Purpose**: Clarify how **MultilingualPress (MLP)** processes internal URLs—particularly those pointing to your Media Library—when you duplicate or translate site content across subsites. While earlier versions of MLP avoided changing post content URLs, more recent releases (MLP 4.9.0+) can automatically update certain media references for **core block editor** content, ensuring copied images remain properly linked in the new site.

---

## Historical Context

In older MLP versions, when you copied or linked content from one language site to another, **no** internal URLs in post content were altered. This approach avoided issues like:

- **No matching “target” content**: A page in the source site might not exist in the target site.
- **Unclear external vs. internal links**: The plugin couldn’t reliably detect if a URL was external or local. Changing an external URL would break it.
- **Potential performance overhead**: Parsing every URL in the post to see if it pointed to an existing remote site page could be resource intensive.
- **Broken media references**: If media were not duplicated, rewriting media URLs would lead to missing images.

---

## Modern Approach (MLP 4.9+)

### 1. Copying Source Content with Core Blocks

For **WordPress block editor** (a.k.a. Gutenberg) posts and pages, MLP now can **replace media URLs** when you use the **“Copy source content”** option in the translation metabox. This includes:

- **Images** in core image blocks
- **Galleries** in core gallery blocks
- **Other core block references** that embed media from your Media Library

When you copy the content, MLP duplicates those media attachments to the **remote site’s** Media Library (if “Copy Attachments” is also selected). It then **updates** the corresponding URLs to ensure images, galleries, or file downloads point to the new site’s uploads.

> **Important**: This automated rewriting only covers **WordPress core block** references. If you use custom or third-party blocks that store media differently, MLP may not detect or change them.

### 2. Classic Editor or Non-Core Content

If content is entered via:

- **Classic Editor** text fields
- **Page builders** or plugin shortcodes
- **Custom-coded references** within post content

MLP does **not** automatically rewrite those URLs. The plugin cannot parse arbitrary HTML or shortcodes reliably without risking broken or external links. In such scenarios:

- Media might not be recognized for duplication.
- The existing media URLs remain pointing to the source site.

### 3. Whole Site Duplication & Media

For **site duplication** (e.g., creating a new site “based on” an existing one):

- MLP can copy the entire Media Library content to the new site if you choose **“Copy attachments”**.
- For pages or posts using the **block editor**, MLP updates embedded references so images point to the newly created media objects in the duplicated site.
- If you have custom logic, classic editor HTML, or external references, those remain unchanged.

---

## Why Not Replace All URLs?

Even with the improved rewriting for block-based media, MLP still won’t alter **arbitrary** links in your content:

1. **Risk of Breaking External Links**
    - Rewriting any URL that might not belong to your source site is dangerous.
2. **Performance Considerations**
    - Doing extensive regex over HTML or other markup can slow site duplication.
3. **No Guarantee of Matching Pages**
    - A URL referencing `example.com/en/page-slug` might not have a counterpart in `example.com/de/`. Overwriting it to `example.com/de/page-slug` may yield a 404 if that page doesn’t exist.

Thus, MLP focuses on **reliably recognized** references—specifically **block-based media** that the plugin knows how to duplicate and link properly.

---

## Best Practices

1. **Use the Block Editor for Media**
    - If your team primarily uses the WordPress block editor for images or file embeds, MLP can gracefully handle duplication.
2. **Check Third-Party Blocks**
    - Custom or page builder blocks might store media references in ways MLP can’t parse. Confirm if your builder or plugin is known to be fully MLP-compatible.
3. **Manual Adjustments**
    - For Classic Editor or older content with raw links, you may need to manually edit or search-replace them in the target site after duplication.
4. **Validate Duplicate Sites**
    - After duplicating a site, quickly preview key pages to confirm images or attachments display correctly.
5. **Contribute to Compatibility**
    - If you find other block types or plugin references that MLP doesn’t yet rewrite but should, share feedback with our support team.

---

## Conclusion

**MultilingualPress 4.9.0+** improves how media URLs are copied for core block editor content—**rewriting** them to the new site’s Media Library references upon duplication. However, links outside the standard block framework remain unchanged, preventing unintentional breakage. By leveraging the block editor and employing MLP’s “Copy Attachments” feature, you can streamline bilingual or multilingual content creation with minimal manual URL fiddling.