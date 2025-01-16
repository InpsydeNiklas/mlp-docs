**Purpose**: Show how to activate Elementor within a WordPress Multisite network and configure MultilingualPress to translate Elementor page content seamlessly.

---

## 1. Install & Activate Elementor

1. **Network Plugin Installation**
    
    - Go to **My Sites → Network Admin → Plugins → Add New**.
    - Search for **Elementor**, install it, and choose **Network Activate** if you want it enabled on all sites.
    - _(Alternatively, you can activate Elementor on individual sites if you prefer.)_
2. **Verify Setup per Site**
    
    - Switch to each site where you need Elementor (**My Sites → [Site Name] → Dashboard**).
    - Complete any initial Elementor setup prompts (if any).

---

## 2. Enable the Elementor Module in MultilingualPress

1. **Open MultilingualPress Modules**
    
    - In the Network Admin, go to **My Sites → Network Admin → MultilingualPress → Modules**.
2. **Activate “Elementor”**
    
    - Check the box next to **Elementor** (or **Elementor Integration**, depending on your MultilingualPress version).
    - Click **Save Changes**.

By enabling this module, MultilingualPress can properly detect and duplicate Elementor page builder data across your network’s translations.

---

## 3. Create & Edit a Page with Elementor

1. **Add a New Page**
    - On one site (e.g., your main or English site), go to **Dashboard → Pages → Add New**.
    - Title your page (e.g., “Elementor Test Page”) and **Save Draft**.
2. **Edit with Elementor**
    - Click **Edit with Elementor** to launch the page builder.
    - Build your layout (e.g., add sections, columns, text, or media).
    - **Update** or **Publish** your changes when finished.

---

## 4. Translate the Elementor Page via MultilingualPress

1. **Return to the WordPress Editor**
    - Exit the Elementor interface to go back to the page’s standard edit screen.
2. **MultilingualPress Translation Metabox**
    - In the **Translation Metabox** for each language, select **Create a new page** (or link an existing one) and choose “Overwrite content” if you want the exact Elementor layout/data copied.
    - Provide a translated title or any immediate text changes you need.
3. **Publish & Verify**
    - **Publish** the original page to complete the duplication process.
    - Switch to each translated site (e.g., Italian or German) and see the automatically duplicated Elementor content. You can then open the page in Elementor to refine the translation further, if desired.

---

## Next Steps

- **Refine Translations**: After duplicating content, you can open each translated page in Elementor to finalize text or media changes in the target language.
- **Sync Advanced Fields**: Explore [ACF Sync](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#) or other advanced modules if your layouts include additional custom fields.
- **Explore More Builders**: MultilingualPress also supports other site builders (e.g., Beaver Builder).

By enabling the **Elementor** module in MultilingualPress, you seamlessly translate or duplicate page layouts across multiple sites—giving each language version the same design while still allowing independent customizations.