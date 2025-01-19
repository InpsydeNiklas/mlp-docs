**Context**  
MultilingualPress offers a “Create a new site based on…” feature that allows you to duplicate an existing WordPress Multisite subsite quickly. This duplication can include content, media, active plugins, and translation links—greatly simplifying setup when launching a new language site or a similar site with minimal differences.

However, some users encounter **process interruptions** during duplication. This article explains **why** such interruptions can happen and provides practical ways to avoid them—particularly when **third-party plugins** introduce redirect behavior or other conflicts.

---

## How Site Duplication Works in MultilingualPress

When creating a new subsite:

1. **Select a Source Site** under “Based on …” in the **Add New Site** screen.
2. MultilingualPress copies site data: posts, pages, taxonomies, settings, and optionally media attachments and plugin activations.
3. If you choose “Activate all plugins that are active on the source site,” those plugins are automatically enabled on the new subsite upon creation.

**Key Benefit**: You get a new site that closely mirrors the source site, with minimal manual setup.

---

## Why Interruptions Occur

### Redirects from Plugin Activation

Some **third-party plugins** perform automatic redirects immediately after they are activated. During duplication:

- MultilingualPress attempts to copy content and media.
- If a plugin in the source site triggers a redirect upon auto-activation on the **new** site, that redirect prematurely **stops** the copy process. This results in incomplete duplication—often failing to replicate media or other site data.

### Host or Configuration Constraints

Other potential factors:

- **Strict Hosting Limitations**: Certain hosts may have lower PHP timeouts or memory limits, cutting off lengthy duplication processes.
- **Plugin Conflicts**: Multiple plugins might conflict at activation, especially if they hook into the same site-creation events.

---

## Recommended Solutions

### 1. Disable Auto-Activation of Plugins

**Uncheck** the option “Activate all plugins that are active on the source site” before clicking **Add New Site**. This prevents any plugin from auto-enabling (and thus from redirecting) during duplication.

1. Create the site as a copy of the source, **without** activating plugins automatically.
2. Let the duplication process finish.
3. **Manually activate** the needed plugins afterward. If any plugin triggers a redirect then, it won’t interrupt the media-copy or site-copy process.

**Pros**: Stops plugin redirects mid-duplication, ensuring a smooth clone.  
**Cons**: Requires you to remember and enable only the plugins you actually need on the new site.

### 2. Use Minimal Plugins During Duplication

If you **must** have plugins auto-activated:

1. Temporarily **deactivate** all but essential plugins on the source site.
2. Perform the site duplication.
3. Reactivate the other plugins post-duplication.

This approach reduces the chance of encountering problematic redirect logic.

### 3. Copy Media Manually if Needed

In rare cases, you may need to:

1. Create the subsite **without copying** or auto-activating source plugins.
2. **Copy the media** using a separate step—like the bulk copy in **Media Library** or via **FTP** manually placing files into the correct `wp-content/uploads/sites/<site-id>/` folder.
3. Re-scan or re-link media if required.

### 4. Check Hosting and Plugin Conflicts

If duplication **continues to fail**:

- Ensure your **hosting** environment meets recommended memory, timeout, and resource parameters for WordPress Multisite.
- **Test** duplication in a staging environment with all plugins disabled except MultilingualPress to see if the issue disappears. This identifies third-party plugin conflicts.

### 5. Contact MultilingualPress Support

For persistent issues, contact the [MultilingualPress support team](https://multilingualpress.org/support/) with details about your environment, hosting, and plugin set. In many cases, hosting or plugin constraints are the underlying cause, and the support team can guide you through best practices or advanced workarounds.

---

## Conclusion

MultilingualPress’s site-duplication feature can streamline the creation of a new language or regional site by copying content, media, and plugin configurations from a source site. Occasionally, **redirects** triggered by plugin activations or hosting constraints can **interrupt** the process.

**Best Practice**: Disable auto-activation of source-site plugins when creating a new site or minimize your active plugins before duplication. If media copying is repeatedly halted, consider manual or post-creation copying steps. By taking these precautions and verifying your hosting limits, you can ensure a **smooth, complete** site duplication experience with MultilingualPress.