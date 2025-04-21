**Purpose**: Demonstrate how to detect the “Copy source content” checkbox being selected in MultilingualPress’s translation metabox—and conditionally execute your own custom logic.

---

## 1. The “Copy Source Content” Option in the Translation Metabox

When you edit or create a post in a **WordPress Multisite** with **MultilingualPress**:

- You’ll see a **translation metabox** for each connected site (one per language).
- Each metabox includes a **“Copy source content”** checkbox. If checked, MultilingualPress copies the entire post content from the source site to the target site’s corresponding post.

This filter-based approach lets you **inject custom code** that triggers only when “Copy source content” is **checked**.

---

## 2. Use the `multilingualpress.sync_post_meta_keys` Filter

MultilingualPress provides a filter called `multilingualpress.sync_post_meta_keys`, which fires while processing metabox options—like “Copy source content.” Here’s an example:

```php
add_filter('multilingualpress.sync_post_meta_keys', function($keysToSync, $context, $request) {

    // Retrieve the array of metabox data from the request.
    $multilingualpress = $request->bodyValue(
        'multilingualpress',
        INPUT_POST,
        FILTER_DEFAULT,
        FILTER_FORCE_ARRAY
    );

    // Identify the remote site and its posted translation data.
    $remoteSiteId = $context->remoteSiteId();
    $translation = $multilingualpress["site-{$remoteSiteId}"] ?? '';

    // Check if "Copy source content" is enabled for this remote site.
    if (!empty($translation) && isset($translation['remote-content-copy']) && $translation['remote-content-copy'] === '1') {
        // "Copy source content" is checked in the metabox.
        // >>> Add your custom code or logic here. <<<
    }

    // Always return $keysToSync (the list of meta keys to sync).
    return $keysToSync;

}, 10, 3);
```

### Explanation

1. **Filter Signature**
    
    ```php
    add_filter('multilingualpress.sync_post_meta_keys', function($keysToSync, $context, $request) {
        // ...
    }, 10, 3);
    ```
    
    - **$keysToSync**: An array of meta keys that MultilingualPress syncs.
    - **$context**: Contains site/post info like `$context->remoteSiteId()`.
    - **$request**: Represents the current request data, including form fields.
2. **Extract MultilingualPress Form Data**
    
    ```php
    $multilingualpress = $request->bodyValue(
        'multilingualpress',
        INPUT_POST,
        FILTER_DEFAULT,
        FILTER_FORCE_ARRAY
    );
    ```
    
    - Pulls the metabox fields from the user-submitted form.
3. **Find the Translation’s “Copy” Status**
    
    ```php
    $remoteSiteId = $context->remoteSiteId();
    $translation = $multilingualpress["site-{$remoteSiteId}"] ?? '';
    ```
    
    - Each site’s translation metabox is under a key like `site-2` or `site-3`.
    - **Check** the `remote-content-copy` key in `$translation`. If it equals `'1'`, “Copy source content” is checked.
4. **Run Your Custom Code**
    
    ```php
    if (!empty($translation) && $translation['remote-content-copy'] === '1') {
        // "Copy source content" is checked — place your logic here!
    }
    ```
    
    - You can do anything: log a message, copy custom fields, trigger external APIs, etc.
5. **Return `$keysToSync`**
    
    - You must return the filter’s original `$keysToSync` array. This ensures MultilingualPress continues its normal meta synchronization.

---

## 3. What Can You Do Here?

When **“Copy source content”** is checked, you might want to:

- **Synchronize Additional Fields**: Copy extra metadata or custom fields from the source post to the target post.
- **Trigger External Actions**: Call external APIs, send notifications, etc.
- **Log or Track**: Add a logging entry whenever content is auto-copied between language sites.

---

## 4. Putting It All Together

1. **Where to Place Code**
    
    - Ideally, in a **custom plugin**. Or, if needed, in your theme’s `functions.php` (though a plugin is more portable).
2. **Test**
    
    - Edit a post in your primary site, open the translation metabox for a connected language site, and **check** “Copy source content.”
    - Publish or update.
    - Confirm your custom code ran (e.g., check debug logs or see if data was copied).
3. **Edge Cases**
    
    - If you’re **not** using the “Copy source content” feature, your code never runs.
    - MultilingualPress must be active and the post properly linked to another site.

---

## Summary

By hooking into the `multilingualpress.sync_post_meta_keys` filter, you can detect exactly when a user **checks** “Copy source content” within the translation metabox. Whether you need to sync custom data, call an API, or simply log the action, this approach ensures your code **runs only** under those specific circumstances—giving you fine-grained control over multilingual workflows.