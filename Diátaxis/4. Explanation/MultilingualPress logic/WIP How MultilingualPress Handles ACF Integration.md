# How MultilingualPress Handles ACF Integration

This document explains _why_ MultilingualPress and ACF work together seamlessly and _how_ the plugin achieves it.

---

## Overview

**Advanced Custom Fields** (ACF) extends WordPress with field groups (text, image, repeater fields, etc.) that attach to posts, pages, or other post types. In a **multisite** with **MultilingualPress**, each subsite can store its own ACF data—but by **activating the ACF module**, MLP synchronizes that data when you create or update translations.

<!-- Note: Reworded for clarity and conciseness. -->

---

## How It Works

1. **ACF Module**
    - Enabling the ACF module in **MultilingualPress → Modules** allows MLP to recognize ACF field groups and their data as candidates for translation or duplication.
    
2. **Common Field Groups**
    - Each subsite must share an **identical** field group structure (field names, field keys, etc.). This is achieved by exporting/importing field groups to ensure the same schema exists on every site.
    
3. **Translation Metabox**
    - The translation metabox gains an extra **ACF** tab or checkbox for “Copy ACF fields.” When checked, MLP copies custom field values from the source post to the target post.
    
4. **Storing & Syncing**
    - MLP uses your existing **ACF**-created fields. It does **not** create new fields automatically. When you “Overwrite content,” MLP queries the source post’s ACF metadata and copies it to the corresponding custom fields in the target post.

<!-- Note: Reworded steps for conciseness and clearer explanations. -->

---

## Benefits of This Approach

- **Granular Control**: Choose whether to sync all fields or handle them individually.
- **Flexible Translation**: Start with duplicated fields, then adjust each subsite’s text for a fully localized approach.
- **Compatibility**: ACF’s internal structure remains untouched, and MLP coordinates how and where data is duplicated.

<!-- Note: Shortened bullet points to make the benefits clearer and more impactful. -->

---

## Common Questions

**1. Do I have to copy fields for every translation?**  
No. The module offers a checkbox so you can choose whether to copy fields. Uncheck it if you want each subsite to have unique content.

**2. What if fields differ between subsites?**  
ACF requires identical field groups (same field keys) for data duplication. If your subsites have different field keys, they won’t map properly.

**3. Is this the same as standard WordPress custom fields?**  
In essence, yes. ACF stores custom fields in WordPress’s `postmeta` table but uses a structured interface. The MLP ACF module simply coordinates data duplication when creating or updating translations.

<!-- Note: Simplified answers for clarity, particularly in **Common Questions** section. Reworded to focus on key points. -->

---

## Key Takeaways

- **Shared Schema**: Each connected subsite needs matching ACF field groups.
- **Selective Overwrite**: You control whether ACF data is duplicated or separately edited.
- **One Click**: The translation metabox’s “ACF” option automates field duplication, reducing manual copy-paste tasks.

By understanding the **why and how**, you can fully leverage the ACF module in MultilingualPress—saving time on consistent, multi-language field management while retaining granular control over each site’s custom fields.

<!-- Note: Streamlined the **Key Takeaways** for better readability and impact. Emphasized the advantages of the approach. -->
