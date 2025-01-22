# How to Create, Connect, and Translate WooCommerce Attributes in a Multilingual Environment with MultilingualPress

**Purpose**: Learn how to create, connect, and translate WooCommerce Attributes (and their Terms) across multiple language sites in a WordPress multisite environment running MultilingualPress.

---

## 1. Create a WooCommerce Attribute on Your Main Site

1. **Open the Product Attributes Screen**
    - In your **main site** dashboard, go to **Products → Attributes**.
2. **Add a New Attribute**
    - Name it (e.g., “color”), set the **slug** to “color,” and click **Add attribute**.
3. **Configure Terms**
    - Click **Configure terms** next to your newly created attribute.
    - Add relevant Terms (e.g., “Blue,” “Gray,” “Green,” “Red,” “Yellow”).

![Create WooCommerce Attributes and Terms](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Create-WooCommerce-Attributes-and-Terms.png)

**Tip**: Each Term you create here corresponds to a color option in your store’s product variations.

---

## 2. Duplicate the Attribute on a Second Language Site

Now set up the **same** attribute (same slug) on your second language site. In this example, we’ll use a Spanish site.

1. **Go to the Spanish Site**
    - Switch to the Spanish subsite in your multisite network (**My Sites → [Spanish Site] → Dashboard**).
2. **Products → Attributes**
    - Create an attribute with the **same slug** (“color”) but enter the translated attribute name (if desired).
    - Click **Add attribute**.
3. **Configure Terms**
    - Click **Configure terms** and add the Spanish equivalents (e.g., “Azul” instead of “Blue”).

![Spanish Attribute](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-Spanish-site.png)

**Important**: The slug must be identical (e.g., “color”) across all language sites for MultilingualPress to link these attributes correctly.

---

## 3. Confirm the Connection via the Same Slug

When attributes across sites share the **same slug** (e.g., “color”), MultilingualPress recognizes them as translations of each other.

![English Attribute Slug](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-English-language-site.png) ![Spanish Attribute Slug](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/WooCommerce-Attribute-in-Spanish-language-site.png)

- **English Site Slug**: “color”
- **Spanish Site Slug**: “color”

---

## 4. Translate Individual Terms with the Translation Metabox

1. **Edit a Term in One Language**
    - For instance, edit “Blue” on the English site.
2. **Scroll to the Translation Metabox**
    - You’ll see an option to find the related Term in the Spanish site for the same attribute slug.
3. **Search & Connect**
    - Type “Az” (for “Azul”), and MultilingualPress will suggest the existing Spanish term.
    - Confirm to link them.

![Translation Metabox Connecting Terms](https://multilingualpress.org/wp-content/uploads/sites/12/2020/11/Translation-Metabox-is-able-to-find-and-connect-the-related-Terms.png)

Once linked, your WooCommerce “color” attribute across the English and Spanish sites are recognized as translations of each other. Products using these attributes can then display the correct color terms in each language.

---

## 5. Troubleshooting Common Issues

### **Problem: Terms Are Not Showing Up on Translated Sites**
- **Solution**: Make sure the terms are properly configured on each language site. If a term is missing from one language, it won’t appear in the translation metabox.

---

## 6. Advanced Use Cases

- **Custom Attributes**: For custom product attributes (e.g., custom product sizes), ensure that these attributes also have matching slugs across language sites. While MultilingualPress works well with standard WooCommerce attributes, custom attributes may require manual linking and syncing of terms.

---

## 7. Multisite Considerations

- **Multisite-Specific Challenges**: When working with a WordPress multisite, ensure that all language sites are properly connected in your network. A common issue is that attributes created on one site might not be visible on others if the multisite setup is not properly configured.
- **Recommendation**: For best results, always ensure that your multisite network is updated to the latest version of WordPress and MultilingualPress to avoid compatibility issues.

---

## Summary & Next Steps

By ensuring both sites share an **identical attribute slug**, MultilingualPress automatically knows to look for matching Terms under the same attribute. You can now easily translate WooCommerce attributes and their Terms, providing a seamless multilingual shopping experience for your customers.

- **Explore Further**:
    - [Getting Started with MultilingualPress](https://multilingualpress.org/docs/getting-started-with-multilingualpress-3/)
    - [Publish and Translate Products in WooCommerce](#)
    - [Translate Other Taxonomies (Categories, Tags) Across Sites](#)

With these steps, you can confidently manage and translate WooCommerce attributes in a Multisite setup—ensuring consistent product variations in all languages.

