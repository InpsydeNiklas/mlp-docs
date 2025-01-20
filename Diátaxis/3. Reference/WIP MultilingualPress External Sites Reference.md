**Scope**: MultilingualPress’s External Sites module enables you to treat **any external website** as a “language site” in your network. This allows you to display a language switcher and **hreflang** attributes pointing to an outside URL—one that is **not** part of your WordPress multisite installation.

---

## 1. What Are External Sites?

An **external site** in MultilingualPress is essentially a **placeholder** for a language version that lives outside your current multisite environment. This placeholder can be added to:

- Your **language switcher** (e.g., in a navigation menu or block), so users can select it just like any other language site in your network.
- The **hreflang** attributes, helping search engines understand the relationship between your internal content and an external webpage for a particular locale.

MultilingualPress treats these external entries as if they were network sites—except the URL points to a domain or path **outside** your WordPress network.

**Benefits**:

1. **Unified Language Switcher**: Users see internal and external translations in one place.
2. **Consistent Hreflang Attributes**: The external site can be automatically flagged with the correct language/locale for SEO.
3. **Optional Auto-Redirect**: When combined with the **Redirection** module, users can be automatically sent to an external site if their browser language or profile matches that external locale.

---

## 2. Activating and Configuring External Sites

### 2.1 External Sites Module

1. **Enable Module**
    
    - In the **Network Admin** → **MultilingualPress** → **Modules** screen, check “External Sites” and **Save Changes**.
    - Once activated, a new **External Sites** panel becomes available in the MultilingualPress admin menu.
2. **Optional Redirection**
    
    - If you want **automatic redirects** to the external site for matching users, also activate the **Redirection** module under MultilingualPress → **Modules**.
    - Only when Redirection is enabled do you see the **“Enable Automatic Redirect”** option while creating/editing an external site.

### 2.2 External Site Settings

When creating or editing an External Site, you’ll have these fields:

- **Site URL** _(required)_: The external website’s address (e.g., `https://www.externaldomain.com`).
- **Site Language Name** _(required)_: An internal label (e.g., “Italian News”) that can also appear in the language switcher.
- **Site Language Locale** _(required)_: The locale code (e.g., `it-IT`) that identifies this site for hreflang and language-switch logic.
- **Enable Hreflang**: Adds a `<link rel="alternate" hreflang="...">` reference pointing to the external URL.
- **Enable Automatic Redirect**: If the Redirection module is active, selecting this will automatically redirect matching users to the external URL whenever they land on a post that references this site.

**Fallback External Redirection**  
When **Enable Automatic Redirect** is active, you can also designate one external site as the global “fallback” if no other language match is found. This option appears under **MultilingualPress** → **Settings** → **Redirection**.

---

## 3. Linking Content to an External Site

### 3.1 In the Translation Metabox

When you edit a post or page (in a subsite that MultilingualPress manages), the **translation metabox** displays any **External Sites** you have defined. Each external site entry provides:

- **Default**: Uses the Site URL from the External Site’s configuration.
- **Custom URL**: You can override it by entering a specific URL in the field next to the external site’s name.

This way, you can have an **article-by-article** or **page-by-page** external URL if needed (e.g., linking to a particular story on an external news site).

### 3.2 Language Switcher Integration

Adding an external site language option to your menu is the same process as adding any standard site:

- In **Appearance** → **Menus** (or via the **Language Menu** block in FSE), you’ll see the external site listed among your other network sites.
- Enable or position it in the language menu.
- Users now see it as a selectable language, and if “Enable Automatic Redirect” is chosen, they may also get redirected automatically if their language matches.

---

## 4. How Hreflang Works with External Sites

If **Enable Hreflang** is checked:

- MultilingualPress generates a `<link rel="alternate" hreflang="xy-XY" href="...">` link in the head for each external site that references the current post or page.
- Search engines interpret this as a **valid alternate** version for the specified language/region—**even though** it’s hosted externally.

---

## 5. Use Cases & Considerations

- **Separate Domain Strategy**: If you maintain a language site on a **completely separate** domain (or hosted platform) and want it recognized in your main site’s language switcher and hreflang references, External Sites is ideal.
- **Redirection**: Combine with the Redirection module for an **automatic** user experience (e.g., Italian users are immediately forwarded to the external Italian site).
- **Mixed Network**: You can have some languages fully in your multisite and other languages partially or entirely external—**all** displayed in the same language switcher.

---

## 6. Summary

**External Sites** in MultilingualPress offer a flexible way to integrate an **outside domain or website** into your multilingual workflow. By assigning a locale, enabling hreflang, and optionally setting up automatic redirection, you give users a consistent, language-aware experience—whether the content resides in your multisite network or beyond it.
