MultilingualPress provides a **ContentRelations** API for establishing relationships (translations) between posts, terms, or comments in different network sites.

## Overview

To connect (relate) content programmatically, you must:

1. **Collect** the site IDs and the corresponding post/term/comment IDs.
2. **Instantiate** (or resolve) the `ContentRelations` API.
3. **Call** the `createRelationship()` method, passing:
    - An associative array of `[siteId => contentId]`.
    - The content **context** (`'post'`, `'term'`, or `'comment'`).

---

## Usage Example

```php
use Inpsyde\MultilingualPress\Framework\Api\ContentRelations;

// 1. Resolve the ContentRelations service.
$api = \Inpsyde\MultilingualPress\resolve(ContentRelations::class);

// 2. Prepare an array of site IDs and content IDs.
$contentIds = [
    1 => 42,   // post ID 42 on site ID 1
    2 => 123,  // post ID 123 on site ID 2
    3 => 321,  // post ID 321 on site ID 3
];

// 3. Create the relationship for "post" context.
$api->createRelationship($contentIds, 'post');
```

### Context Parameter

- **`'post'`**: Used for standard posts, pages, or any custom post type.
- **`'term'`**: For taxonomy terms (e.g., categories, tags) across languages.
- **`'comment'`**: For connecting comments in a multisite setup.

---

## Notes & Best Practices

1. **Prerequisite**: Make sure each site already has the required content with valid IDs.
2. **Updates**: If you later change an ID or remove a post, you may need to adjust or delete the relationship accordingly.
3. **Consistency**: Ensure the context aligns with how you intend to use or display translations (e.g., do not pass `'post'` for terms).
4. **Dependency Injection**: Depending on your setup, you might retrieve `ContentRelations` differently (e.g., via a DI container). The `resolve()` call in the example uses MultilingualPress’s internal container.

---

## Related References

- [Programmatic Translation Access](#) – Learn how to retrieve translations and their language metadata.
- [MLP Hooks & Filters](#) – Customize behavior (e.g., default metabox states) via code.
- [WP Multisite Overview](https://developer.wordpress.org/advanced-administration/multisite/) – WordPress Multisite basics.

By leveraging the **ContentRelations** API, you can seamlessly connect content across multiple sites—establishing custom translation relationships outside of the WordPress admin UI.