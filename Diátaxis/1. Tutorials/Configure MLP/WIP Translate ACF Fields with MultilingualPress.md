**Purpose**: Quickly enable and use the ACF module in MultilingualPress so that custom fields built with the _Advanced Custom Fields_ plugin can be translated or synced across subsites in a WordPress Multisite.

---

## Prerequisites

- A **WordPress Multisite** network.
- **MultilingualPress** (v3.5 or higher) installed and network activated.
- **Advanced Custom Fields** (ACF) installed and network activated on the subsites where you’ll use custom fields.
- Two or more **connected subsites** in MultilingualPress (e.g., EN and IT).

---

## 1. Activate the ACF Module in MultilingualPress

1. **Go to Network Admin**
    - **My Sites → Network Admin → MultilingualPress → Modules**
2. **Check “ACF”**
    - Click **Save Changes**.
    - If you see the ACF module is “disabled,” confirm that ACF is installed and activated on the network.

---

## 2. Create and Distribute Your ACF Field Groups

1. **Define Fields on One Subsite**
    - On your main site, go to **Dashboard → Custom Fields → Add New**.
    - Create a **Field Group** (e.g., “Proverbs Group”) and add your desired fields (e.g., a “Proverb” text area).
2. **Export Field Group**
    - Go to **Custom Fields → Tools** (on the main site).
    - Check your field group (e.g., “Proverbs Group”) and select **Export File**.
3. **Import on Other Sites**
    - Switch to each connected subsite (e.g., the Italian site).
    - **Custom Fields → Tools → Import**, upload the exported file, then click **Import File**.
    - Now each site has the identical field group and can store data for the same custom fields.

---

## 3. Enter and Translate Content

1. **Create a New Post**
    - On your main site, create a new post or edit an existing one.
    - Fill in the ACF field(s) (e.g., “Proverb”).
2. **Use the MultilingualPress Translation Metabox**
    - Scroll to the translation metabox for each connected subsite.
    - Select **Create a new post** if a translation does not yet exist, and check **Overwrite ACF fields** (or similarly named option) if you want to duplicate the field data.
3. **Publish**
    - Clicking **Publish** (or **Update**) on the original post will create/overwrite the custom field content on each connected subsite.

You can now view the translated post on each subsite to confirm the ACF fields have been duplicated or synced as needed.

---

## 4. Verify & Refine

- **Check Each Subsite**: Confirm the new post or page has the custom field data.
- **Adjust Content**: If you prefer each subsite to have unique data, uncheck the “Overwrite” option or manually edit the fields on each site.

---

### Next Steps

- **Advanced Usage**: Learn how to selectively sync or not sync certain fields.
- **Troubleshooting**: If the ACF module is not visible, ensure ACF and MultilingualPress are updated to compatible versions.
- **Other Custom Fields**: For non-ACF custom fields, see our [Custom Fields How-To](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#).

With these steps, you can efficiently translate or duplicate ACF-created fields across multiple languages—simplifying content management for more complex field structures.
