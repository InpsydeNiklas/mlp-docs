# How to Publish New Content and Manage Translations with MultilingualPress

**Purpose**: This guide walks authors through publishing new content on a primary language site and then creating and managing translations across connected language sites using MultilingualPress.

**Prerequisites**:

- A WordPress Multisite network set up with MultilingualPress, configured for multiple languages (e.g., English, Italian, German).
- Translation relationships between sites have been established.
- Necessary content types and taxonomies are marked as translatable in global settings.

---

## 1. Publish New Content on the Source Site

1. **Log in** to the admin dashboard of your primary language site (e.g., English).
2. Go to **Posts → Add New**.
3. Create a new post:
    - Enter the title and content.
    - Assign relevant categories and tags.
4. Click **Publish** to make the post live on the source site.

---

## 2. Translate Categories and Tags

Translating taxonomies ensures consistency across language sites.

1. **Edit a category or tag** associated with your post on the source site.
2. Scroll down to the **MultilingualPress translation metabox** for other languages.
3. For each target language (e.g., Italian, German):
    - Select **Create a new term, and use it as translation**.
    - Switch to the **Term** tab.
    - Enter the translated name.
    - Click **Update** to create the translated term.
4. Repeat for all categories and tags used in the post.

---

## 3. Create Translations for the Post

1. While editing your source post, scroll to the bottom to find **MultilingualPress translation metaboxes** for each connected language.
2. For each target language (e.g., Italian, German):
    1. In the respective metabox, select **Create a new Post, and use it as translation in [Language]**.
    2. Expand the **Title and Content** tab:
        - Enter the new post title for the target language.
        - Optionally check the box to duplicate the English content.
    3. Expand the **Advanced** tab:
        - Set the desired post status (e.g., Publish).
    4. Expand the **Taxonomies** tab:
        - Check the boxes to select the translated categories and tags created earlier.
3. Click **Update** to create linked translations for each selected language.

---

## 4. Edit Translated Content on Target Sites

1. Log in to a target language site (e.g., Italian).
2. Navigate to the newly created translated post.
3. Replace any duplicated English content with the actual translated text.
4. Update and publish the post if necessary.

---

## 5. Verify Translations

- **Check Front-End**: Visit each language version of the post to ensure that translations, categories, and tags display correctly.
- **Use Language Switcher**: Navigate between language versions using your site’s language switcher to verify proper linking.

---

## Troubleshooting Common Issues *(New Section)*

### **Problem: **
- **Solution**: 

---

## How to Go Further

- **Explore Quicklinks**: Activate and configure Quicklinks in MultilingualPress settings to improve navigation between translations.
- **Practice**: Try creating content and translations starting from different language sites to deepen your understanding.
- **Consult Documentation**: For advanced features, troubleshooting, and deeper insights, refer to the [official MultilingualPress documentation](https://multilingualpress.org/docs-category/multilingualpress-3/).

---

By following these steps, authors can efficiently publish new content and manage translations across multiple languages using MultilingualPress, making the most of WordPress Multisite’s multilingual capabilities.
