MultilingualPress integrates with WP-CLI to allow executing certain actions more efficiently in a WordPress multisite setup.

> **More Details**: For a comprehensive list of flags and advanced usage, see **CLI-COMMANDS.md** in the MultilingualPress repository.

---

## 1. Requirements

- **WordPress Multisite**: 5.0 or higher
- **PHP**: 8.0 or higher
- **MultilingualPress**: Installed and network-activated
- **WP-CLI**: Installed on your server or development environment

---

## 2. Overview

The MLP-CLI commands extend WP-CLI to handle common MultilingualPress tasks:

- Manage **languages** for each site
- Manage **content relations** (posts, terms, comments)
- Manage **site relations**, including creating new sites with MLP-specific options
- Manage **modules** (activate/deactivate)
- Manage **licenses** (activate/deactivate)

All commands support the standard WP-CLI global flags. Commands requiring confirmation can be auto-confirmed with the `--yes` flag.

---

## 3. Commands by Category

### 3.1 Language Management

#### **Set Site Language**

Use this command to assign a specific language (locale) to a site. For instance, you might assign `es-ES` to a site with ID `4`:

```shell
wp mlp setLanguage --site-id=4 --language=es-ES
```

> **Tip**: You can combine this with other WP-CLI flags like `--url=<site_url>` if needed.

---

### 3.2 Content Relations

#### **Posts**

- **Create Relation**
    
    ```shell
    wp mlp relations post create \
      --source-site-id=<id> --source-entity-id=<post_id> \
      --target-site-id=<id> --target-entity-id=<post_id>
    ```
    
- **Delete Relation**
    
    ```shell
    wp mlp relations post delete \
      --source-site-id=<id> --source-entity-id=<post_id> \
      --target-site-id=<id> --target-entity-id=<post_id>
    ```
    
- **List Relations**
    
    ```shell
    wp mlp relations post list <post_id>
    wp mlp relations post list <post_id> --url=<site_url>
    ```
    

#### **Terms**

- **Create Relation**
    
    ```shell
    wp mlp relations term create \
      --source-site-id=<id> --source-entity-id=<term_id> \
      --target-site-id=<id> --target-entity-id=<term_id>
    ```
    
- **Delete Relation**
    
    ```shell
    wp mlp relations term delete \
      --source-site-id=<id> --source-entity-id=<term_id> \
      --target-site-id=<id> --target-entity-id=<term_id>
    ```
    
- **List Relations**
    
    ```shell
    wp mlp relations term list <term_id>
    wp mlp relations term list <term_id> --url=<site_url>
    ```
    

#### **Comments**

> **Note**: Requires the **Comments** module active in MultilingualPress.

- **Create Relation**
    
    ```shell
    wp mlp relations comment create \
      --source-site-id=<id> --source-entity-id=<comment_id> \
      --target-site-id=<id> --target-entity-id=<comment_id>
    ```
    
- **Delete Relation**
    
    ```shell
    wp mlp relations comment delete \
      --source-site-id=<id> --source-entity-id=<comment_id> \
      --target-site-id=<id> --target-entity-id=<comment_id>
    ```
    
- **List Relations**
    
    ```shell
    wp mlp relations comment list <comment_id>
    wp mlp relations comment list <comment_id> --url=<site_url>
    ```
    

---

### 3.3 Site Relations & Creation

- **Connect Sites**
    
    ```shell
    wp mlp relations site connect <site_id_1> <site_id_2>
    ```
    
- **Disconnect Sites**
    
    ```shell
    wp mlp relations site disconnect <site_id_1> <site_id_2>
    ```
    
- **List Site Relations**
    
    ```shell
    wp mlp relations site list <site_id>
    ```
    

#### **Create a New Site with MLP-Specific Arguments**

This command wraps the core `wp site create` function, adding extra MLP options:

- `--mlp-language=<locale>` (e.g., en-US)
- `--relations=<site_ids>` (e.g., 1,2,3)
- `--based-on=<site_id>` plus optional flags:
    - `--copy-attachments`
    - `--connect-content`
    - `--connect-comments`
    - `--activate-plugins`
    - `--copy-users`

**Example**:

```shell
wp mlp site create \
  --slug=example \
  --title="Example Site" \
  --mlp-language=en-US \
  --relations=1,2,3 \
  --based-on=1 \
  --connect-content \
  --activate-plugins \
  --copy-users
```

- **List Network Sites (With MLP Info)**
    
    ```shell
    wp mlp site list
    ```
    

---

### 3.4 Modules

Enable or disable specific MultilingualPress modules:

- **Activate a Module**
    
    ```shell
    wp mlp module activate <module_slug>
    ```
    
- **Deactivate a Module**
    
    ```shell
    wp mlp module deactivate <module_slug>
    ```
    

> Common modules include `woocommerce`, `comments`, `redirect`, and `gutenberg_blocks`.

---

### 3.5 License

Manage the MultilingualPress license via the command line:

- **Activate**
    
    ```shell
    wp mlp license activate --api-key=<ABC> --product-id=<123>
    ```
    
- **Deactivate**
    
    ```shell
    wp mlp license deactivate
    ```
    

---

## 4. Tips & Best Practices

- **Use `--yes`** for unattended scripts or CI/CD pipelines:
    
    ```shell
    wp mlp relations post delete --source-site-id=1 --target-site-id=2 --yes
    ```
    
- **Combine commands** with native WP-CLI flags like `--url=<site_url>` to target specific subsites.
- **Check Module Dependencies**: For example, `comments` commands require the Comments module to be active.
- **See Also**: The [CLI-COMMANDS.md](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#) file in the MultilingualPress repository for an exhaustive list of arguments and examples.

---

## 5. Further Resources

- [WP-CLI Official Documentation](https://make.wordpress.org/cli/handbook/)
- [MultilingualPress Docs](https://chatgpt.com/g/g-p-677ffd6da894819197dd7cf3a90d93fa-mlp-docs/c/6780001b-80d8-8011-8739-903a6ccdb99d#)
- [Creating a Network](https://developer.wordpress.org/advanced-administration/multisite/create-network/)

By using MLP-CLI, you can streamline multilingual site management—configuring site languages, linking posts or terms across sites, and managing modules or licenses—all from the command line.