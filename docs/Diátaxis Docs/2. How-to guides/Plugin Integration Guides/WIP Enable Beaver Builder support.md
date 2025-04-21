# How to Enable Beaver Builder Support in a Multilingual WordPress Setup with MultilingualPress

**Purpose**: Learn how to activate Beaver Builder for a WordPress Multisite and configure MultilingualPress to translate pages built with Beaver.

---

## 1. Install & Activate Beaver Builder

1. **Network Plugin Installation**
    - Go to **My Sites → Network Admin → Plugins → Add New**.
    - Search for **Beaver Builder**, install, and **Network Activate** if you want it available on all sites.
    - _(Alternatively, you can activate Beaver Builder on specific sites only.)_

2. **Verify Setup on Each Site**
    - For each site using Beaver Builder, switch to **My Sites → [Site Name] → Dashboard**.
    - Complete any initial Beaver Builder prompts if required.

**Tip**: Beaver Builder helps you create visually engaging layouts. Enabling it across sites ensures that your content can be easily duplicated and translated with MultilingualPress.

---

## 2. Enable the Beaver Builder Module in MultilingualPress

1. **MultilingualPress Modules**
    - From the **Network Admin**, navigate to **My Sites → Network Admin → MultilingualPress → Modules**.

2. **Activate “Beaver Builder”**
    - Check the box next to **Beaver Builder**.
    - Click **Save Changes**.

MultilingualPress is now aware of Beaver Builder data when duplicating or translating pages.

---

## 3. Create & Edit a Page with Beaver Builder

1. **Add a New Page**
    - In one site (e.g., your English site), go to **Dashboard → Pages → Add New**.
    - Give it a title (e.g., “Beaver Builder Test Page”) and **Save Draft**.

2. **Launch Beaver Builder**
    - Click **Launch Beaver Builder** (or a similar button, depending on your setup).
    - Use Beaver Builder’s drag-and-drop tools to create your layout (e.g., columns, text blocks, embedded video).
    - Save and exit back to the WordPress editor when finished.

---

## 4. Translate the Beaver Builder Page via MultilingualPress

1. **Open the Translation Metabox**
    - In the WordPress editor, scroll down to the **MultilingualPress** translation metabox for each target language (e.g., Italian, German).

2. **Create the New Translated Page**
    - Under **Relationship** (or similar tab), choose **Create a new page** for each language.
    - Under **Title and Content**, enter a translated title and check **Overwrite content on translated post** if you want to copy the Beaver Builder layout into the translated page.

3. **Publish & Verify**
    - Click **Publish** on the original page.
    - MultilingualPress will duplicate the Beaver Builder content in the target sites, preserving columns, text, media, etc.

_(Optional)_

- **Refine in Beaver Builder**: Switch to each translated site, open the duplicated page in Beaver Builder, and fine-tune any localized text or images.

---

## 5. Troubleshooting Common Issues

### **Problem: Content Not Appearing on Translated Pages**
- **Solution**: Ensure that the **Overwrite content on translated post** box is checked in the translation metabox.

### **Problem: Beaver Builder Layout Not Duplicating Properly**
- **Solution**: Ensure both **Beaver Builder** and **MultilingualPress** plugins are updated to the latest versions. Check that all necessary modules in MultilingualPress are activated.

---

## 6. Compatibility Considerations

- Some WordPress themes might not fully support Beaver Builder layouts, which could affect how the page is displayed after translation. Be sure to test the translated pages to ensure they appear correctly.

---

## 7. Next Steps

- **Explore Further**: If your page includes custom fields, see [ACF Sync](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#) or other advanced sync settings in MultilingualPress.
- **Translate Other Builders**: Similar steps apply to [Elementor](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#), which MultilingualPress also supports.
- **Enhance Workflows**: Use [Language Menus](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#) or Quicklinks to let users quickly switch among translated pages.

With Beaver Builder support enabled, you can effortlessly duplicate and customize complex page layouts for each language site in your WordPress multisite—offering a seamless, visually consistent experience across all locales.
