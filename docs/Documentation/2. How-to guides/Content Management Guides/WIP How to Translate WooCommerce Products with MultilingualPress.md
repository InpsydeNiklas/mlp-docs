**Purpose**: Learn how to translate and link WooCommerce products across language sites in your WordPress Multisite network using MultilingualPress.

---

## Prerequisites

- A WordPress Multisite network with **MultilingualPress** and **WooCommerce** installed
- The WooCommerce module enabled in the global MultilingualPress settings
- Global MultilingualPress settings configured to mark WooCommerce content types and taxonomies (e.g., Products, Coupons, Orders, Product Categories, and Product Tags) as translatable

---

## Steps to Translate WooCommerce Products

### 1. Verify Global Settings

Before translating products, ensure that all necessary WooCommerce content types and taxonomies are enabled for translation:

1. Navigate to **My Sites → Network Admin → MultilingualPress → Settings**.
2. Under **Translatable Post Types** and **Translatable Taxonomies**, select all WooCommerce-related items you want to translate (e.g., Products, Product Categories, Product Tags).
3. Save changes.

---

### 2. Open a Product for Translation

1. Go to the admin dashboard of a site containing WooCommerce products.
2. Navigate to **Products → All Products** and select a product to edit.
3. Scroll down below the product editor to find the **MultilingualPress Translation Metaboxes** for each connected language site.

---

### 3. Link or Create Translations

Within each language-specific translation metabox:

1. **Link Existing Product** or **Create a New Product**: Choose the appropriate option based on whether you already have a translation or need to create one.
2. Fill in fields like **New Post Title**, **URL**, and select relevant checkboxes to copy source content, images, etc., as needed.

---

### 4. Utilize the Product Data Tab

Each WooCommerce product translation metabox includes a **Product Data** tab. This tab offers options tailored to different product types and common product settings. Use these options to copy specific product details from the source to the translation:

#### For Simple Products:

- **Price Fields**: Check boxes to copy **Regular Price** and **Sale Price**.
- **Downloadable Options**: Enable checkboxes to copy downloadable files and settings.
- **Upsells & Cross Sells**: Select options to copy related products (ensure those products exist and are linked on the destination site).

#### For Grouped Products:

- Use checkboxes to copy **Grouped** product settings and link Upsell products.

#### For External/Affiliate Products:

- Enable copying of **Product URL** and **Button Text** for affiliate products.

#### For Variable Products:

- Select checkboxes to copy **Attributes** and **Variations** between translations.

#### Common Options Across Product Types:

- **Product Type**: Change the product type on the remote site.
- **SKU and Inventory Settings**: Copy SKU, manage stock, stock quantity, backorder settings, low stock threshold, sold individually options.
- **Gallery and Descriptions**: Copy gallery images, product short description, and purchase note.
- **Inventory Settings Override**: Override remote product inventory with source product settings.

---

### 5. Finalize and Save

After selecting all relevant options in the translation metabox:

1. Click **Save** or **Update** to apply changes and create or update the translation on the connected language site.
2. Repeat for other products or languages as needed.

---

## Additional Considerations

- **Pre-Existing Product Links**: For options like Upsells, Cross Sells, Grouped Products, ensure that the related products exist and are connected on the destination site before copying.
- **Stock and Inventory**: Remember that WooCommerce shops on individual sites maintain independent inventory; MultilingualPress links products but does not share stock information.
- **Central Stock Plugin**: If you need a centralized inventory system across language sites, consider using our specialized plugin [Central Stock for WooCommerce](https://wp-centralstock.com/).

---

By following these steps, you can effectively translate WooCommerce products, ensuring that product data, pricing, downloadable options, and related items are properly replicated or linked across multiple language sites in your network.