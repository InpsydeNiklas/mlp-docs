MultilingualPress provides several APIs to fetch translated content—either as fully detailed “Translation” objects or as arrays of connected post IDs. Below is a concise overview of available methods and their typical usage patterns.

---

## 1. Using the `Translations` Class (Detailed Objects)

### 1.1 Overview

You can retrieve detailed translation data (including language metadata) using the `Translations` service, configured via the `TranslationSearchArgs` class. Each returned translation includes the post ID, URL, title, and associated `Language` object.

### 1.2 Key Classes

- **`\Inpsyde\MultilingualPress\Framework\Api\TranslationSearchArgs`**  
    Builds arguments (e.g., site ID, include base post, etc.) for the query.
- **`\Inpsyde\MultilingualPress\Framework\Api\Translations`**  
    Executes the search and returns an array of `Translation` objects.

### 1.3 Sample Code

```php
use Inpsyde\MultilingualPress\Framework\Api\TranslationSearchArgs;
use Inpsyde\MultilingualPress\Framework\Api\Translations;
use Inpsyde\MultilingualPress\Framework\WordpressContext;

add_filter('the_content', function($content) {
    // Build TranslationSearchArgs
    $args = TranslationSearchArgs::forContext(
        new WordpressContext()
    )
    ->forSiteId(get_current_blog_id()) // Filter by current site
    ->includeBase();                   // Include the source post itself

    // Resolve the Translations service and run the query
    $translations = resolve(Translations::class)->searchTranslations($args);

    // Each $translation is a Translation object
    foreach ($translations as $translation) {
        $postId = $translation->remoteContentId();
        $title  = $translation->remoteTitle();
        $url    = $translation->remoteUrl();
        
        // Language info
        $language = $translation->language();
        $bcp47tag = $language->bcp47tag();
        // ... etc.
    }

    return $content;
});
```

### 1.4 Returned Translation Data

- **`remoteContentId()`**: The numeric ID of the translated post.
- **`remoteTitle()`**: The post title.
- **`remoteUrl()`**: The post’s URL.
- **`language()`**: Returns a `Language` object, exposing methods for locale info (`bcp47tag()`, `isoCode()`, `name()`, etc.).

---

## 2. Using the `translationIds()` Function (Connected Post IDs)

### 2.1 Overview

The function `translationIds()` is the **modern equivalent** of `mlp_get_linked_elements` (MultilingualPress 2). Rather than returning full “Translation” objects, it gives you a **simple mapping of site IDs to content IDs** (or term IDs, comment IDs, etc.).

### 2.2 Function Signature

```php
/**
 * Retrieves connected content IDs for the given source content.
 *
 * @param int    $sourceId   The source post/term/comment ID.
 * @param string $type       One of 'post', 'term', or 'comment'.
 * @param int    $sourceSite The source site ID.
 *
 * @return array Associative array of [siteId => contentId].
 */
\Inpsyde\MultilingualPress\translationIds($sourceId, $type, $sourceSite);
```

### 2.3 Example Usage

```php
use function Inpsyde\MultilingualPress\translationIds;

// Retrieve all connected “post” translations for post ID 1 on site ID 1.
$translations = translationIds(1, 'post', 1);

/**
 * Example return:
 * array(
 *   1 => 1,
 *   2 => 5,
 *   3 => 12
 * )
 */
if ($translations) {
    foreach ($translations as $siteId => $postId) {
        echo "Site ID: {$siteId}, Post ID: {$postId}<br>";
    }
}
```

> **Note**: For `$type`, you can pass `'post'`, `'term'`, or `'comment'` to query the appropriate translations.

---

## 3. Notes and Best Practices

1. **Dependency Injection**: If you’re using a DI container, ensure you call `resolve()` for the `Translations` class. Otherwise, you may need to instantiate it directly (depending on your setup).
2. **Filtering Options**: With the `Translations` service, you can chain methods like `->forContentId()`, `->excludeCurrentSite()`, `->includeBase()`, etc., to fine-tune results.
3. **Use Cases**:
    - **Detailed Objects**: If you need language metadata or remote URLs for display.
    - **Simple Arrays**: If you only need site IDs → content IDs mapping, for looping or redirect logic.

---

## 4. Further Resources

- [API Overview & Hooks](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)
- [MLP Dependency Injection Setup](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)
- [Tutorial: How to Programmatically Manage Translations](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)

By leveraging these two approaches—`Translations` for detailed data and `translationIds()` for connected IDs—you can efficiently retrieve and process multilingual content relationships in your WordPress multisite network.