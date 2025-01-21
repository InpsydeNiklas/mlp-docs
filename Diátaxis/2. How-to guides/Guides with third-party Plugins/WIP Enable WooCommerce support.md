# How to Enable WooCommerce Support in a Multilingual WordPress Setup with MultilingualPress

**Purpose**: Guide users through activating WooCommerce in a multisite environment and configuring MultilingualPress to translate WooCommerce products and taxonomies.

---

## 1. Install & Activate WooCommerce

1. **Install WooCommerce**
    - In your WordPress Network Admin, go to **My Sites → Network Admin → Plugins → Add New**.
    - Search for **WooCommerce**, install, and **Network Activate** if you want it enabled across all sites.
    - _(Alternatively, you can activate WooCommerce only on specific sites.)_

2. **Verify WooCommerce Setup**
    - Switch to each site using WooCommerce (e.g., **My Sites → [Site Name] → Dashboard**).
    - Complete any initial WooCommerce setup steps if prompted (e.g., store address, currency, etc.).

**Tip**: Enabling WooCommerce across your multisite network ensures that your e-commerce store is ready for multilingual content. MultilingualPress makes it easy to manage translations of product content across sites.

---

## 2. Enable the WooCommerce Module in MultilingualPress

1. **Open MultilingualPress Modules**
    - From the Network Admin, go to **My Sites → Network Admin → MultilingualPress → Modules**.

2. **Activate “WooCommerce”**
    - Check the box next to **WooCommerce** (or **WooCommerce Integration**, depending on your plugin version).
    - Click **Save Changes**.

This step ensures that MultilingualPress can detect and properly handle WooCommerce product data when translating and duplicating content across languages.

---

## 3. Verify “Products” and WooCommerce Taxonomies are Translatable

1. **Go to MultilingualPress Settings**
    - In the Network Admin, navigate to **My Sites → Network Admin → MultilingualPress**.

2. **Select “Translatable Post Types” Tab**
    - Ensure **Products** (or **product**) is checked.

3. **Select “Translatable Taxonomies” Tab**
    - Ensure **Product categories** and **Product tags** are checked.

This ensures that your WooCommerce products and related taxonomies will be properly translated across different language sites.

---

## 4. Manage Translations from the Product Edit Screen

With WooCommerce support enabled, you’ll see **MultilingualPress translation metaboxes** in the product edit screen on each language site. These let you:

- Link products across languages.
- Duplicate or translate product descriptions, attributes, and taxonomies.
- Keep data in sync (or separate) as needed when updating a product.

---

## 5. Troubleshooting Common Issues

### **Problem: Product Descriptions Aren't Duplicating Across Sites**
- **Solution**: Ensure that the product is linked correctly via the MultilingualPress translation metabox and that all product fields are set as translatable.

### **Problem: Product Categories or Tags Aren’t Syncing**
- **Solution**: Check that the **Product categories** and **Product tags** are marked as translatable in the MultilingualPress settings.

---

## 6. Compatibility Considerations

- **Theme and Plugin Compatibility**: Some WordPress themes or additional plugins may not fully support the translation of WooCommerce products and taxonomies. If you notice issues with how products are displayed after translation, try switching to a default theme to see if the issue persists.
- **Custom Fields**: If your products use custom fields, ensure that they are properly synced across sites.

---

## 7. Next Steps

- **Connect and Translate WooCommerce Attributes**: Learn how to align product attributes (e.g., color, size) across languages.
- **Translate Product Categories & Tags**: Ensure your store’s taxonomy structure is consistent across all sites.
- **Advanced Synchronization**: Explore MultilingualPress settings for syncing custom fields, comments, or user roles.

With WooCommerce support enabled, you’re ready to create and manage multilingual e-commerce products across your network—providing a fully translated shopping experience for customers around the world.
