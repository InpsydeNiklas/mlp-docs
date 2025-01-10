**Purpose**: Walk you through creating a custom post type (CPT) and taxonomy on one site, replicating them on another, and translating/connecting them across multiple languages.

---

## 1. Prerequisites

1. A **WordPress Multisite** installation with at least two sites connected via MultilingualPress (e.g., English and German).
2. **MultilingualPress** (version 3 or higher) installed and network activated.
3. A plugin or method to create CPTs/taxonomies:
    - For this example, we’ll use the free [Custom Post Type UI](https://wordpress.org/plugins/custom-post-type-ui/) plugin.

### Before You Begin

- If you need to set up a WordPress Multisite, see [How to Install and Set Up a WordPress Multisite](https://multilingualpress.org/docs/how-to-install-wordpress-multisite/).
- If you haven’t yet connected your sites in MultilingualPress, follow [Getting Started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/).

---

## 2. Install & Activate Custom Post Type UI

1. **Decide on Network or Individual Site Activation**
    - CPT UI does **not** have full Multisite support in its free version, so we recommend activating it on each site you’ll use it on.
2. **Activate in Each Site**
    - From the **Network Admin** dashboard, switch to each subsite (e.g., **My Sites → [Site Name] → Dashboard → Plugins**).
    - Install and **Activate** **Custom Post Type UI**.

> **Note**: If you register your CPT via **PHP code** (using `register_post_type`), ensure the code runs on each site or is set to run network-wide.

---

## 3. Create a Custom Post Type & Taxonomy

We’ll illustrate with a **“Recipes”** CPT and an **“Ingredients”** taxonomy on our **English** site.

1. **Go to the English Site Dashboard**
    - **CPT UI → Add/Edit Post Types**.
2. **Create a CPT**
    - Under “Add New Post Type,” specify:
        - **Slug**: `recipes` (or another slug).
        - **Plural Label**: “Recipes”
        - **Singular Label**: “Recipe”
        - Adjust any other options as desired.
    - Click **Add Post Type**.
3. **Create a Taxonomy**
    - **CPT UI → Add/Edit Taxonomies**.
    - For **Ingredients**:
        - **Slug**: `ingredients`
        - **Plural Label**: “Ingredients”
        - **Singular Label**: “Ingredient”
        - Associate it with the “recipes” post type.
    - Click **Add Taxonomy**.

Your English site now has a “Recipes” CPT and an “Ingredients” taxonomy.

---

## 4. Copy CPT/Taxonomy to Other Sites

We need the _same_ CPT and taxonomy definitions on the German site (or any other language site). With CPT UI, you can **export** and **import** settings:

1. **Export from Site 1 (English)**
    - **CPT UI → Tools**
    - Under **Export Post Types**, copy the JSON/code for “Recipes.”
    - Under **Export Taxonomies**, copy the JSON/code for “Ingredients.”
2. **Import into Site 2 (German)**
    - Switch to the German site dashboard.
    - **CPT UI → Tools**
    - Paste the exported code in **Import Post Types** and click **Import**.
    - Paste the taxonomy code in **Import Taxonomies** and click **Import**.

> **Alternate Method**: If you manually register via `register_post_type` or `register_taxonomy`, replicate the code for each site (or create a network-wide plugin that runs the registration code on all sites).

---

## 5. Enable CPT & Taxonomy in MultilingualPress Settings

1. **Open Network Admin**
    - **My Sites → Network Admin → MultilingualPress → Settings**.
2. **Translatable Post Types**
    - In the **Translatable Post Types** tab, check **Recipes** (or your CPT).
3. **Translatable Taxonomies**
    - In the **Translatable Taxonomies** tab, check **Ingredients** (or your taxonomy).
4. **Save Changes**
    - Now MultilingualPress knows to treat these as translatable content.

---

## 6. (Optional) Translate Slugs

If you want a localized slug (e.g., `rezepte` in German), see our separate guide: [How to Translate Post Type and Taxonomy Slugs](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#). You can do this either by providing a custom rewrite slug in CPT UI or editing it in **MultilingualPress → Post Type Slugs**.

---

## 7. Create & Translate CPT and Taxonomy Content

### 7.1 Add Taxonomy Terms

1. **On the English Site**
    - **Recipes → Ingredients** (the newly created taxonomy).
    - Add terms like “Tomato,” “Chicken,” “Garlic,” etc.
2. **In the Translation Metabox**
    - After creating or editing a term, scroll down to the **MultilingualPress** translation metabox.
    - Choose **Create a new term** on the German site or **Select an existing term** if it already exists.
    - Repeat for all necessary terms.

### 7.2 Add CPT Posts

1. **On the English Site**
    - Go to **Recipes → Add New**.
    - Create “Garlic Chicken” or any recipe. Assign relevant taxonomy terms (e.g., “Chicken,” “Garlic”).
2. **Use the Translation Metabox**
    - **Create a new recipe** in German or link to an existing one.
    - (Optional) In the **Advanced** tab, select **Copy featured image** or other sync options.

---

## 8. Verify Language Switching

1. **Menus/Language Switcher**
    - Each site needs a language menu or switcher to navigate between translations.
    - _Appearance → Menus_ (or use a **Language Menu Block** if you prefer).
2. **Test**
    - View a “Recipes” post on the English site.
    - Click the German language switcher link.
    - You should land on the translated “Rezepte” post (assuming you linked or created it via the translation metabox).

---

## 9. Manage Permalinks

- **Recommended**: Use pretty permalinks (e.g., `/recipes/chicken-dish/`).
- **Check**: If you see `/blog/` in your permalink structure (common in fresh Multisite setups), remove it by re-saving permalinks or editing the structure on each site.
- **Save Permalinks** again on each site after making changes to the CPT rewrite or slug to ensure URLs are refreshed.

---

## Summary & Next Steps

**Congratulations!** You’ve successfully created a custom post type and taxonomy on multiple language sites and enabled their translations in MultilingualPress. Users can navigate between translations in the front end, and the same content structure (Recipes + Ingredients) is available on each site.

- **Further Customization**:
    - [How to Translate Post Type and Taxonomy Slugs](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#) for localized rewrite rules.
    - [Syncing Additional Fields](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#) if you use ACF or other custom fields.
    - Explore **Advanced** MLP features like [Automatic Redirects](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#), [Quicklinks](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#), or [Language Menus](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#).

With this approach, you can adapt _any_ custom post type or taxonomy to a multilingual setup—giving you granular control over how posts, terms, and slugs appear across various language sites in your network.