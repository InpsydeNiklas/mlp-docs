**Purpose**: Learn how to modify the default options in the MultilingualPress translation metabox—such as automatically copying the source content, featured image, or synchronizing taxonomies—by using simple code snippets.

---

### 1. Understand What Can Be Filtered

MultilingualPress provides filters to control the **default state** (checked/unchecked) of several translation-metabox options, as well as the available post statuses:

1. **Copy source content**
2. **Copy featured image**
3. **Synchronize Taxonomies**
4. **ACF fields**
5. **Post Status** (limit available statuses)

> **Not Filterable**: Title, excerpt, edit link, and WooCommerce-specific fields (e.g., WC product data).

---

### 2. Add the Code Snippets to Your Site

To change any default value, you’ll need to add custom PHP code. You can do this in your theme’s `functions.php` file or via a custom plugin. If you want to experiment with code snippets without modifying your theme or creating a custom plugin, you can use the aptly named [Code Snippets plugin](https://wordpress.org/plugins/code-snippets/).

Below are examples of each filter ready to copy and paste.

---

#### 2.1. Automatically Copy the Source Content

```php
/**
 * Filters the "checked" state of the "Copy source content" checkbox.
 * 
 * @return bool if true the checkbox should be checked by default, otherwise it will be unchecked.
 */
add_filter('multilingualpress.copy_content_is_checked', static function (bool $checked): bool {
    return true;
});
```

#### 2.2. Automatically Copy the Featured Image

```php
/**
 * Filters the "checked" state of the "Copy featured image" checkbox.
 *
 * @return bool if true the checkbox should be checked by default, otherwise it will be unchecked.
 */
add_filter('multilingualpress.copy_featured_image_is_checked', static function (bool $checked): bool {
    return true;
});
```
---

#### 2.3. Synchronize Taxonomies by Default

```php
/**
 * Filters the "checked" state of the "Synchronize Taxonomies" checkbox.
 *
 * @return bool if true the checkbox should be checked by default, otherwise it will be unchecked.
 */
add_filter('multilingualpress.copy_taxonomies_is_checked', static function (bool $checked): bool {
    return true;
});
```

---

#### 2.4. Limit or Set Available Post Statuses

```php
/**
 * Filters the available list of statuses for the "status" field.
 *
 * @param string[] $statues The list of available statuses. ('draft', 'pending', 'publish', 'future')
 *
 * @return string[] The list of available statuses.
 */
add_filter('multilingualpress.translation_ui_post_statuses', static function (array $statues): array {
    return ['publish'];
});
```

> **Note**: You can also include multiple statuses, e.g., `return ['draft', 'publish'];`.

---

#### 2.5. Automatically Copy ACF Fields

```php
/**
 * Filters the "checked" state of the "Copy ACF Fields" checkbox.
 *
 * @return bool if true the checkbox should be checked by default, otherwise it will be unchecked.
 */
add_filter('multilingualpress.copy_custom_fields_is_checked', static function (bool $checked): bool {
    return true;
});
```

---

### 3. Verify the Changes

1. **Edit Any Post/Page**: Open a post or page in any MultilingualPress-enabled site.
2. **Scroll Down to the Translation Metabox**:
    - Confirm that your default checkboxes (e.g., “Copy source content,” “Synchronize Taxonomies,” etc.) are now preselected or deselected as intended.
    - Check that the status dropdown includes only the statuses you’ve defined.

If your changes are not reflected, clear your cache (if using a caching plugin) and ensure your code snippets are in the correct location without syntax errors.

---

### Next Steps

- **Refine Your Setup**: Combine multiple filters to customize each translation-metabox option exactly the way you need.
- **Explore Advanced Hooks**: Check out other [MultilingualPress hooks and filters](#) for more advanced customization.
- **Manage WooCommerce Fields**: If you’re working with WooCommerce, see [our guide on enabling WooCommerce support](#) to manage product data across languages.

By adjusting these default values, you can save time and ensure a consistent translation workflow—helping your team quickly spin up new language versions with the right options already in place.