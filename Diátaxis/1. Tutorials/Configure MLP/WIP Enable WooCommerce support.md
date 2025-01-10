**Purpose**: Guide users through activating WooCommerce in a multisite environment and configuring MultilingualPress to translate WooCommerce products and taxonomies.

---

### 1. Install & Activate WooCommerce

1. **Install WooCommerce**
    
    - In your WordPress Network Admin, go to **My Sites → Network Admin → Plugins → Add New**.
    - Search for **WooCommerce**, install, and **Network Activate** if you want it enabled across all sites.
    - _(Alternatively, you can activate WooCommerce only on specific sites.)_
2. **Verify WooCommerce Setup**
    
    - Switch to each site using WooCommerce (e.g., **My Sites → [Site Name] → Dashboard**).
    - Complete any initial WooCommerce setup steps if prompted (e.g., store address, currency, etc.).

---

### 2. Enable the WooCommerce Module in MultilingualPress

1. **Open MultilingualPress Modules**
    - From the Network Admin, go to **My Sites → Network Admin → MultilingualPress → Modules**.
2. **Activate “WooCommerce”**
    - Check the box next to **WooCommerce** (or **WooCommerce Integration**, depending on your plugin version).
    - Click **Save Changes**.

---

### 3. Verify “Products” and WooCommerce Taxonomies are Translatable

1. **Go to MultilingualPress Settings**
    - In the Network Admin, navigate to **My Sites → Network Admin → MultilingualPress.
2. **Select “Translatable Post Types”** Tab
    - Ensure **Products** (or **product**) is checked.
3. **Select “Translatable Taxonomies”** Tab
    - Ensure **Product categories** and **Product tags** are checked.

---

### 4. Manage Translations from the Product Edit Screen

With WooCommerce support enabled, you’ll see **MultilingualPress translation metaboxes** in the product edit screen on each language site. These let you:

- Link products across languages.
- Duplicate or translate product descriptions, attributes, and taxonomies.
- Keep data in sync (or separate) as needed when updating a product.

---

### Next Steps

- **Connect and Translate WooCommerce Attributes**: Learn how to align product attributes (e.g., color, size) across languages.
- **Translate Product Categories & Tags**: Ensure your store’s taxonomy structure is consistent across all sites.
- **Advanced Synchronization**: Explore MultilingualPress settings for syncing custom fields, comments, or user roles.

With WooCommerce support enabled, you’re ready to create and manage multilingual e-commerce products across your network—providing a fully translated shopping experience for customers around the world.