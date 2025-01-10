**Purpose:** Add a new WordPress site in your multisite network for an additional language, and configure MultilingualPress options for translations.

### 1. Access the Network Admin

1. In your WordPress dashboard, go to:  
    **My Sites** → **Network Admin** → **Sites**
2. This screen displays all the sites in your network—either in subdomains or subdirectories, depending on your network setup.

### 2. Add a New Site

1. Click **Add New** at the top of the **Sites** screen.
2. Fill in the required fields:
    - **Site Address** (URL-friendly name; only a-z, 0-9, and hyphens allowed)
    - **Site Title** (the new site’s title)
    - **Site Language** (the WordPress language to use for admin menus, etc.)
    - **Admin Email** (the email address for this site’s administrator)

### 3. Configure MultilingualPress Settings

Under **MultilingualPress Settings** (usually at the bottom of the “Add Site” form), you can fine-tune how this new site connects to your existing network sites:

- **Language**  
    Assign the language that MultilingualPress will associate with this site for features like automatic hreflang attributes and redirection.
- **Relationships**  
    Choose whether to connect this new site to existing sites that are assigned different languages. This allows you to link content (posts, pages, terms) between them.
- **Based on Site**  
    If you want to replicate an existing site’s settings and content, select that site here. You can also choose from various duplication options:
    - **Copy Attachments**: Duplicate the existing site’s Media Library items
    - **Connect Content**: Set up relationships between existing posts/pages and their new counterparts
    - **Connect Comments**: Merge comments between the original and the new site
    - **Plugins**: Enable the same plugins active on the original site
    - **Users**: Add the same user roles and permissions

> **Tip:** If you only need a bare-bones new site, leave the “Based on Site” options disabled. If you want a head start with content, enable them.

### 4. Finalize

Click **Add Site** to create the new site. The process usually completes within seconds, depending on site size and server performance.

1. You’ll see a success message.
2. Click **Visit Dashboard** to jump into the newly created site.

---

**Next Steps:** [Publish New Content in Multiple Languages](#publish-new-content-in-multiple-languages)