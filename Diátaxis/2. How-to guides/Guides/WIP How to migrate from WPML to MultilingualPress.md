# How to Migrate from WPML to MultilingualPress

This guide explains how to migrate your multilingual WordPress site from **WPML** to **MultilingualPress (MLP)**. This migration will ensure that all content, translations, and language settings are preserved and properly structured within a **WordPress Multisite** environment with MLP.

---

## **1. Prerequisites**

Before starting the migration, ensure that:

- You have **admin access** to your WordPress installation.
- You have **backed up your website** (database and files).
- Your site is currently using **WPML** for multilingual content.
- You have installed and activated **MultilingualPress** on a **WordPress Multisite** setup.

---

## **2. Exporting Content from WPML**

Since WPML stores translations differently than MultilingualPress, we need to export each language separately using our **WPML WXR Exporter** plugin.

### **2.1 Install the WPML WXR Exporter**

1. Download and install the **WPML WXR Exporter** plugin.
2. Activate the plugin in WordPress.

### **2.2 Exporting Content for Each Language**

1. Go to `Tools → WPML Export`.
2. The **current language** will be automatically detected.
3. **Select the post types** to export:
    - Posts
    - Pages
    - Products (if WooCommerce is active)
4. Click **Download WXR Export**.
5. Repeat the process for each language.

---

## **3. Setting Up MultilingualPress**

1. Ensure that **Multisite** is properly configured.
2. **Create a subsite for each language** in the network.
    - Example:
        - **Main Site:** English (`example.com` or `example.com/en`)
        - **Subsite:** German (`example.com/de`)
        - **Subsite:** French (`example.com/fr`)
3. Install and **activate MultilingualPress** network-wide.
4. Go to `Network Admin → Sites` and **assign a language** to each subsite using MLP settings.

---

## **4. Importing Content into MultilingualPress**

Now, we will import each **language’s exported WXR file** into the respective MultilingualPress subsite.

### **4.1 Importing Content**

1. Log in to the **subsite** where you want to import content.
2. Go to `Tools → Import` and select **WordPress Importer**.
3. Click **Run Importer** and upload the WXR file for that language.
4. Assign authors if prompted and complete the import.
5. Repeat for each language subsite.

### **4.2 Verifying Imported Content**

- Ensure that all **posts, pages, and products** are imported correctly.
- Check that content is assigned to the **correct language subsite**.
- Verify that **media files** have been imported correctly.

---

## **5. Linking Translations in MultilingualPress**

After importing, we need to **link translations** manually in MLP.

### **5.1 Linking Content Across Sites**

1. Go to `Posts` (or `Pages`, or `Products`) in a subsite.
2. Edit a post that has a translation in another subsite.
3. Locate the **MultilingualPress Translation Box**.
4. Select the corresponding post/page in another subsite.
5. Click **Save**.
6. Repeat for all translated posts/pages.

### **5.2 Setting Up Language Switcher**

1. Go to `Appearance → Widgets`.
2. Add the **MultilingualPress Language Switcher** widget.
3. Configure the settings and save.
4. Alternatively, use `[mlp_language_switcher]` shortcode.

---

## **6. Final Checks**

- ✅ Ensure **all translations are correctly linked**.
- ✅ Test **language switcher navigation**.
- ✅ Verify **permalinks and redirects**.
- ✅ Run an **SEO audit** to confirm correct hreflang settings.

---

## **7. Post-Migration Cleanup**

Once everything is verified, you can safely:

- **Deactivate WPML**.
- **Remove any old WPML language settings**.
- **Enable MLP-specific multilingual SEO settings**.

---

## **8. Summary**

✅ Export WPML content **language-by-language**.  
✅ Import each **WXR file into its corresponding MLP subsite**.  
✅ **Link translations manually** in MLP.  
✅ **Test and verify everything** before finalizing the migration.

---

**🎉 Congratulations! Your site is now successfully migrated to MultilingualPress!**