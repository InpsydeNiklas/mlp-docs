# Media Handling in a WordPress Multisite with MultilingualPress

**Purpose**: This article explains how WordPress Multisite manages media by default—each subsite having its own library—and how **MultilingualPress (MLP)** simplifies working with media files in multilingual networks. We’ll discuss both the underlying pros and cons of the default approach and how MultilingualPress’ features help you avoid some of the hassle typically associated with separate media libraries.

---

## Default Media Libraries in WordPress Multisite

By default, each **WordPress Multisite** subsite stores uploaded images, videos, and documents in its own folder under `wp-content/uploads/sites/<ID>/`. WordPress also displays only the local site’s files in that subsite’s Media Library screen.

- **Independent File Metadata**: Each site can maintain unique file titles, alt text, or descriptions (key for multilingual usage).
- **Local Permissions**: An editor on subsite #2 won’t see or manipulate media from subsite #3 by default.

**Why Separate Libraries?**

- **Localization**: Different language versions of an image can have separate translations for alt text or file titles.
- **Site Autonomy**: Subsites can deviate or replace brand assets freely without affecting others.

<!-- Note: This section remains mostly the same, providing a clear overview of the default media libraries. Clarified the purpose of having separate media libraries (localization and site autonomy). -->

---

## Pros & Cons of Per-Site Media

### Pros

1. **Local Language Metadata**
    
    - Each subsite can store alt text, captions, or product images in the correct language.
    - Great for multilingual commerce: shipping labels, disclaimers, or legally mandated differences can be easily maintained.
2. **Flexibility for Regional Markets**
    
    - Distinct subsite libraries ensure that each region or language site can provide region-specific visuals or compliance images as needed.
3. **Clarity of Ownership**
    
    - Helps large networks track who uploaded what, since admins on one subsite do not overlap with another subsite’s media.

### Cons & Mitigations

1. **Repeated Media for Shared Assets**
    
    - If many sites use the same logo, each library has a copy. This can bloat hosting space.
    - **MLP Benefit**: If images need to be copied during content duplication, MLP handles attachments in a structured, predictable way—rather than random manual uploads.
2. **Editing Shared Assets**
    
    - Without special setup, updating a shared image across multiple sites can require multiple edits.
    - **Workaround**: In some networks, administrators keep brand assets in one “master” library or use a plugin like Network Media Library for a global repository. MLP provides simpler duplication but does not forcibly unify libraries.
3. **No Automatic Sync**
    
    - If you want identical media changes across all translations simultaneously, that is not natively provided in WordPress.
    - **Recommendation**: Evaluate advanced solutions if your assets frequently change. However, for most multilingual sites, partial autonomy is beneficial.

<!-- Note: Added clarification on the benefits of MLP in handling repeated media and editing shared assets. Also, included a **workaround** for using Network Media Library in cases where media syncing across subsites is needed. -->

---

## How MultilingualPress Eases Media Management

### 1. Copy Media Library When Creating a New Language Site

When you create a subsite “based on” an existing one, **MultilingualPress** can:

- **Duplicate Site**: Copy all posts, pages, and **attachments** to the new site’s library.
- **Result**: Eliminates manual re-uploads and ensures each local library has the same starting set of images or documents.

**Why This Is Helpful**:

- Kickstart a new language version with the same brand assets or product images.
- Edits remain site-specific afterward, letting local teams alter or replace assets without messing up the original.

<!-- Note: Explained how MLP helps with duplicating media when creating a new site. Could benefit from a **screenshot** showing the "based on" site creation process. -->

### 2. Copy Attachments for Core Blocks

For the **block editor** (Gutenberg), MLP can automatically rewrite internal media URLs when copying a post’s content:

- **Core WordPress Blocks** (e.g., Image, Gallery, File blocks) are recognized.
- **MLP** duplicates the referenced media and updates the embedded media URL so it points to the new site’s library.

**Benefit**: Translated or duplicated posts remain fully functional with images intact—no references to the old site with image metadata in the wrong language.

<!-- Note: This section could benefit from a **screenshot** showing how media URLs are rewritten when posts are duplicated using the Gutenberg block editor. This would help users visualize the process. -->

### 3. Media Copying in the Editor and Across the Network

- **On-Demand Attachment Copy**: MLP’s features allow you to copy attachments from one subsite to another if you wish to unify content.
- **Reduced Confusion**: Instead of manually downloading and re-uploading the same image, MLP helps replicate it into the target subsite library.

<!-- Note: Added a practical example to clarify how MLP helps users avoid re-uploading media. A **screenshot** of the media copying process in the editor could be useful here to further illustrate the point. -->

### 4. Future-Focused Architecture

MLP’s approach to media duplication lines up with WordPress best practices—**no** overwriting or hooking into every raw image reference. Instead, only recognized block-based references are updated, preventing accidental rewrites of external or non-media links.

<!-- Note: This section provides important technical info about MLP’s architecture. While not necessary, an **architecture diagram** could clarify how MLP handles media without affecting external links. -->

---

## Recommendation: Keep Libraries Separate, Leverage MLP Features

1. **Per-Site Libraries**: Maintain local file metadata, ensuring each language’s alt text, legal disclaimers, or brand visuals suit local needs.
2. **Use MLP for Duplication**: When creating new language sites or duplicating content, rely on MLP’s **“Copy Attachments”** and block-based URL rewriting for minimal overhead.
3. **Optional Global Solutions**: If your organization truly needs a single asset bank, consider advanced plugins like **Network Media Library**. Yet, this can compromise local autonomy.
4. **Validate Post-Copy**: Always confirm important pages or e-commerce listings after duplication. MLP typically handles block references well, but custom or third-party blocks may need a manual check.

<!-- Note: Added more context and clarification around **per-site libraries** and the **validation process**. This section is more user-centered with a focus on simplicity. -->

---

## External Tools for Specialized Cases

- **Network Media Library**: Merges subsite uploads into a single global media library.
- **AMF WordPress**: Offloads or hosts media externally, still letting each site appear to have local media.
- **Custom CDNs or S3 Offloads**: More advanced solutions for large networks needing cost-effective or globally cached media hosting.

<!-- Note: Added recommendations for advanced solutions in case a global repository is required. **Screenshots** or **images** of the interfaces for these plugins (e.g., **Network Media Library**) could make it easier for users to compare these solutions visually. -->

---

## Conclusion

With WordPress Multisite’s **default** design, each site uses a distinct media library—**MultilingualPress** embraces that separation while smoothing duplication, rewriting internal references for block-based content, and allowing site-level autonomy for truly multilingual workflows. Combined with MLP’s site duplication features, you can launch new language sites, copy existing media, and keep your brand consistent—without losing the flexibility to customize or localize each library.

<!-- Note: The conclusion summarizes the key points but could include a **final screenshot** demonstrating the end-to-end media management workflow, including duplication and URL rewriting, to wrap up the explanation visually. -->