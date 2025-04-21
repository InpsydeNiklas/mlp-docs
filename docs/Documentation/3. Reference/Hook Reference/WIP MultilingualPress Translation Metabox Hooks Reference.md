Below is a **concise reference** for MultilingualPress **Translation Metabox** hooks. These filters let you adjust default options—such as whether to copy source content, featured images, or taxonomies—for new translations. The minimal code examples show typical usage. For further details or how-to instructions, see the full [Customize the Default Values in the Translation Metabox](#) tutorial.

---

## MultilingualPress Translation Metabox Hooks

### 1. `multilingualpress.copy_content_is_checked`

**Purpose**  
Determines if the “Copy source content” checkbox is selected by default.

```php
add_filter('multilingualpress.copy_content_is_checked', function (bool $checked): bool {
    return true; // or false
});
```

### 2. `multilingualpress.copy_featured_image_is_checked`

**Purpose**  
Determines if the “Copy featured image” checkbox is selected by default.

```php
add_filter('multilingualpress.copy_featured_image_is_checked', function (bool $checked): bool {
    return true; // or false
});
```

### 3. `multilingualpress.copy_taxonomies_is_checked`

**Purpose**  
Determines if the “Synchronize Taxonomies” checkbox is selected by default.

```php
add_filter('multilingualpress.copy_taxonomies_is_checked', function (bool $checked): bool {
    return true; // or false
});
```

### 4. `multilingualpress.translation_ui_post_statuses`

**Purpose**  
Defines which post statuses appear in the translation metabox dropdown (e.g., `draft`, `publish`).

```php
add_filter('multilingualpress.translation_ui_post_statuses', function (array $statuses): array {
    return ['draft', 'publish'];
});
```

### 5. `multilingualpress.copy_custom_fields_is_checked`

**Purpose**  
Determines if the “Copy ACF Fields” checkbox is selected by default.

```php
add_filter('multilingualpress.copy_custom_fields_is_checked', function (bool $checked): bool {
    return true; // or false
});
```

---

**Note**: These filters should be placed in a custom plugin or your theme’s `functions.php`. When you update or re-deploy your site, confirm the filters remain active and test their behavior by editing a post’s translation metabox.