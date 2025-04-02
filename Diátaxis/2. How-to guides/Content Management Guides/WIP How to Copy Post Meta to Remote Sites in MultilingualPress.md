**Purpose**: Demonstrate how to programmatically copy or synchronize a post meta key/value pair from a source site to one or more remote sites when creating or editing translations via MultilingualPress.

---

## 1. Prerequisites

1. **WordPress Multisite** with two or more sites connected via MultilingualPress.
2. **MultilingualPress** plugin (>3.x+) properly installed and network activated.
3. Comfort writing custom PHP code, typically in a custom plugin or your theme’s `functions.php`.

---

## 2. Understand the Hook: `multilingualpress.metabox_after_relate_posts`

MultilingualPress fires the `multilingualpress.metabox_after_relate_posts` action **after** the user has defined how a post on the source site relates to a post on the remote site. By hooking into this action, you can:

- Read values from the **source** post (e.g., a Yoast SEO title or a custom field).
- Switch to the **remote** site, where you retrieve or update the corresponding post meta.
- Switch back to the source site (if needed).

**Key parameters** (passed to your callback):

- `$context` (object): Contains info like `sourceSiteId()`, `sourcePostId()`, `remoteSiteId()`, `remotePostId()`.
- `$request` (object): Allows you to read data from the user’s form submission (or request body).

---

## 3. Example 1: Copy Yoast SEO Title (`_yoast_wpseo_title`)

In this example, we assume the plugin or theme has registered the `_yoast_wpseo_title` meta field on your posts. When you relate a post to a remote site in the MultilingualPress translation metabox, the code below:

1. Reads `yoast_wpseo_title` from the request.
2. Switches to the **remote** site.
3. Updates the meta value `_yoast_wpseo_title` on the remote post.

```php
add_action('multilingualpress.metabox_after_relate_posts', function($context, $request) {

    // 1. Read the Yoast SEO title from the request.
    $yoastWpseoTitleValue = (string) $request->bodyValue(
        'yoast_wpseo_title',
        INPUT_POST,
        FILTER_SANITIZE_SPECIAL_CHARS
    );

    // 2. Switch to the remote site.
    $remoteSiteId = $context->remoteSiteId();
    $remotePostId = $context->remotePostId();
    switch_to_blog($remoteSiteId);

    // 3. Update the meta value on the remote post.
    update_post_meta($remotePostId, '_yoast_wpseo_title', $yoastWpseoTitleValue);

    // 4. Switch back.
    restore_current_blog();

}, 10, 2);
```

**Usage Notes**:

- This code reads the value from the **form request** rather than from the database. If you prefer reading from the **source post’s database** directly, see Example 2 below.
- The meta key (`_yoast_wpseo_title`) must match Yoast SEO’s internal naming.

---

## 4. Example 2: Copy Custom Fields Registered in the Editor

If you’ve created a custom field in the **source** site (e.g., `my-field`) and want to push it to the **remote** site’s post meta, follow this pattern:

1. **Switch** to the source site to get the meta value from the database.
2. **Switch** back to the remote site to write that value.

```php
add_action('multilingualpress.metabox_after_relate_posts', function ($context, $request) {
    // 1. Switch to the source site.
    switch_to_blog($context->sourceSiteId());
    // 2. Grab post meta from the source post.
    $value = get_post_meta($context->sourcePostId(), 'my-field', true);
    // 3. Switch back to the original site.
    restore_current_blog();

    // 4. Switch to the remote site (optional: if needed after restore_current_blog()).
    switch_to_blog($context->remoteSiteId());
    // 5. Update the same field name on the remote post.
    update_post_meta($context->remotePostId(), 'my-field', $value);
    restore_current_blog();
}, 10, 2);
```

**Preparation**:

- Ensure both sites have the **same custom field name** (e.g., `my-field`) in the post editor, or it exists in the code that registers that meta field.

---

## 5. Implementation Tips

- **Where to Place This Code**:
    - Ideally in a **custom plugin** to keep your changes portable and avoid losing them during theme updates.
- **Version Control**:
    - Manage your plugin or `functions.php` in a repo if you maintain multiple environments.
- **Security**:
    - Always sanitize or validate the user’s input. Here, we use `FILTER_SANITIZE_SPECIAL_CHARS` or read from the database after `switch_to_blog()`.
- **Testing**:
    - Create a test post on the source site, fill the custom field, and relate it to a new or existing post on the remote site.
    - Confirm the meta appears on the remote post (in the database or via the post editor UI).

---

## 6. Next Steps & Advanced Usage

- **Multiple Fields**: You can replicate this approach for multiple custom fields. Just repeat the `get_post_meta()` and `update_post_meta()` logic for each field key.
- **Selective Overwrites**: If you only want to overwrite data when the remote field is empty, add a condition around `update_post_meta()`.
- **ACF or Other Plugins**: The principle is the same for advanced field plugins—just use the meta keys they store.

By implementing this hook-based strategy, you can ensure that custom or plugin-defined post meta stays synchronized across sites whenever you create or update translations with MultilingualPress—making your multilingual content management more seamless and efficient.