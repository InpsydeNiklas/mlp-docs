## **Context**

MultilingualPress provides a **“Create a new site based on…”** feature that allows users to duplicate an existing WordPress Multisite subsite quickly. This duplication process can include copying content, media, active plugins, and translation links—streamlining setup when launching a new language site or a site with similar characteristics.

However, some users encounter **process interruptions** during duplication. This article explains the common reasons behind these interruptions and offers practical solutions, particularly when **third-party plugins** introduce redirect behaviors or conflicts that interfere with the duplication process.

---

## **How Site Duplication Works in MultilingualPress**

To create a new subsite using the duplication feature:

1. **Select a Source Site** under the “Based on …” option in the **Add New Site** screen.
2. MultilingualPress copies site data, including posts, pages, taxonomies, settings, and optionally media attachments and plugin activations.
3. If you choose to “Activate all plugins that are active on the source site,” those plugins are automatically enabled on the new subsite.

**Key Benefit**: The duplication process creates a new site that mirrors the source site with minimal manual setup required.

---

## **Why Interruptions Occur**

### **Redirects from Plugin Activation**

Some **third-party plugins** trigger automatic redirects immediately upon activation. During duplication:

- MultilingualPress attempts to copy content and media.
- If a plugin in the source site triggers a redirect upon auto-activation on the **new** site, that redirect prematurely **stops** the copy process. This results in incomplete duplication—often failing to replicate media or other site data.

### **Host or Configuration Constraints**

Other potential factors:

- **Strict Hosting Limitations**: Certain hosts may have lower PHP timeouts or memory limits, cutting off lengthy duplication processes.
- **Plugin Conflicts**: Multiple plugins might conflict at activation, especially if they hook into the same site-creation events.

---

## **Recommended Solutions**

### **1. Disable Auto-Activation of Plugins**

**Uncheck** the option “Activate all plugins that are active on the source site” before clicking **Add New Site**. This prevents any plugin from auto-enabling (and thus from redirecting) during duplication.

1. Create the site as a copy of the source, **without** activating plugins automatically.
2. Let the duplication process finish.
3. **Manually activate** the needed plugins afterward. If any plugin triggers a redirect then, it won’t interrupt the media-copy or site-copy process.

**Pros**: Stops plugin redirects mid-duplication, ensuring a smooth clone.  
**Cons**: Requires you to remember and enable only the plugins you actually need on the new site.

### **2. Use Minimal Plugins During Duplication**

If you **must** have plugins auto-activated:

1. Temporarily **deactivate** all but essential plugins on the source site.
2. Perform the site duplication.
3. Reactivate the other plugins post-duplication.

This approach reduces the chance of encountering problematic redirect logic.

### **3. Copy Media Manually if Needed**

In rare cases, you may need to:

1. Create the subsite **without copying** or auto-activating source plugins.
2. **Copy the media** using a separate step—like the bulk copy in **Media Library** or via **FTP** manually placing files into the correct `wp-content/uploads/sites/<site-id>/` folder.
3. Re-scan or re-link media if required.

### **4. Check Hosting and Plugin Conflicts**

If duplication **continues to fail**:

- Ensure your **hosting** environment meets recommended memory, timeout, and resource parameters for WordPress Multisite.
- **Test** duplication in a staging environment with all plugins disabled except MultilingualPress to see if the issue disappears. This identifies third-party plugin conflicts.

### **5. Contact MultilingualPress Support**

For persistent issues, contact the [MultilingualPress support team](https://multilingualpress.org/support/) with details about your environment, hosting, and plugin set. In many cases, hosting or plugin constraints are the underlying cause, and the support team can guide you through best practices or advanced workarounds.

---

## **Conclusion**

MultilingualPress’s site-duplication feature can streamline the creation of a new language or regional site by copying content, media, and plugin configurations from a source site. Occasionally, **redirects** triggered by plugin activations or hosting constraints can **interrupt** the process.

**Best Practice**: Disable auto-activation of source-site plugins when creating a new site or minimize your active plugins before duplication. If media copying is repeatedly halted, consider manual or post-creation copying steps. By taking these precautions and verifying your hosting limits, you can ensure a **smooth, complete** site duplication experience with MultilingualPress.
