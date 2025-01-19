# MultilingualPress and WordPress Editors: Compatibility and Focus

**Purpose**: This explanation outlines how MultilingualPress handles various WordPress editors and page builders. While our plugin remains compatible with the Classic Editor and other popular site builders, MultilingualPress development focuses primarily on the modern, block-based WordPress Editor (Gutenberg)—ensuring a clean, future-ready approach to creating multilingual content.

---

## From Classic Editor to the Modern WordPress Editor

1. **Classic Editor**:
    
    - Historically, WordPress provided a WYSIWYG editing experience without “blocks.” Many site owners still rely on this editor for simplicity or legacy reasons.
    - **MultilingualPress Support**:
        - Fully usable with Classic Editor. If you’re continuing to rely on the pre-WordPress 5.0 editing style, rest assured MLP synchronizes content in the same reliable way, including translation relationships and duplication features.
2. **Gutenberg (Block Editor)**:
    
    - Introduced in WordPress 5.0, it rethinks content creation around _blocks_ (text, images, embeds, etc.).
    - **MultilingualPress Focus**:
        - MLP 3+ was designed with the block editor in mind—no additional plugins or add-ons required.
        - MLP’s translation metaboxes or block-based “Language Menu” blocks help you create and link multilingual content without interfering in the block editing process.
3. **Full Site Editing (FSE) Themes**:
    
    - FSE extends the block paradigm to entire site layouts—headers, footers, templates, etc.
    - **MLP’s Approach**:
        - We aim to ensure that block-based site editing remains seamless across translated sites, focusing on providing intuitive solutions for global or per-language block structures.

---

## MultilingualPress & Page Builders

While the block editor is our core development focus, many site owners prefer advanced page-builder plugins for more granular design controls:

### 1. Elementor

- **MLP Compatibility**:
    - Once you enable the **Elementor** module in MultilingualPress (if needed), you can duplicate the content built with Elementor.
    - MLP respects each site’s design configurations, letting you maintain unique or similar layouts across languages.

### 2. Beaver Builder

- **MLP Compatibility**:
    - Similar to Elementor, Beaver Builder can be used to create complex layouts for each language site.
    - MLP ensures block-based or builder-based designs remain independent, offering translation linking through standard MLP controls.

### 3. WPBakery (Visual Composer), Bricks, Cornerstone, etc.

- **General Principles**:
    - If a page builder saves content in standard WordPress fields and post meta, MLP can typically duplicate or link that data across language sites.
    - Certain specialized fields or shortcodes might need additional mapping—feedback from users helps us enhance and refine advanced compatibility.

### 4. Ongoing Development & Feedback

- **Priority**:
    - Ensuring each language site loads only the necessary builder assets, preserving performance and stability.
    - Our team listens to user experiences—if you encounter issues with a builder, we welcome your feedback to improve or add deeper integration.

---

## Why Our Primary Focus Is the Block Editor

- **Core WordPress**: The block-based approach is now a standard WordPress feature, increasingly adopted by theme developers.
- **Performance & Future-Readiness**: A single code baseline for editing experiences helps keep your multilingual content lean, portable, and free from lock-in.
- **UX Consistency**: The block editor provides a consistent UI for content creation, letting MLP integrate seamlessly for language switching and translation linking.

---

## Classic Editor & Legacy Support

- **Continuing Legacy Projects**: If you maintain older sites or prefer the Classic Editor for workflow reasons, **MultilingualPress** remains compatible.
- **Enterprise Environments**: Some organizations rely on older editorial processes or custom post flows—MLP does not force you to adopt the block editor. You can always install the [Classic Editor plugin](https://wordpress.org/plugins/classic-editor/) network-wide or individually, and MLP translations remain unaffected.

---

## Summary

MultilingualPress 4.9+ is fully compatible with:

- **Modern WordPress Editor** (Gutenberg blocks, Full Site Editing themes).
- **Classic Editor** if you choose to retain the older workflow.
- **Popular Page Builders** like Elementor, Beaver Builder, WPBakery, Bricks, and others, provided you activate them per site or network-wide as needed.

**Our Development Focus** remains on the WordPress block paradigm for performance, code cleanliness, and user experience, while we also maintain broad compatibility with page builders. We welcome your input if you encounter any special needs or incompatibilities, as user feedback drives improvements in our ongoing goal to deliver the most flexible and future-proof multilingual solution.