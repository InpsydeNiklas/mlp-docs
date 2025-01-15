**Purpose**: Learn how to add a new website to your WordPress Multisite network, set its language, and configure MultilingualPress settings to integrate it into your multilingual ecosystem.

---

## Step 1: Add a New Website to the Network

1. Navigate to **My Sites → Network Admin → Sites**.
    
2. Click the **Add New** button.
    
    ![Add a new website to the network](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/multilingualpress-network-sites.png)
    

---

## Step 2: Configure General Site Settings

On the **Add New Site** page, fill in the standard multisite information:

- **Site Address (URL)**: Enter the URL slug for your new website.
- **Site Title**: Provide a descriptive title.
- **Site Language**: Choose the backend language for the new site.
- **Admin Email**: Specify the administrator's email.

    ![General settings for new site](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/add-new-site-to-wordpress-multisite.png)
    

These settings are part of WordPress Multisite setup and not specific to MultilingualPress.

---

## Step 3: Configure MultilingualPress Settings for the New Site

Below the general settings, you will find a section for MultilingualPress-specific options:

- **Language**:  
    Select the primary content language for the new site (e.g., French). This setting affects hreflang URLs and language-related features.
    
- **Relationships**:  
    Link this new site with other language sites in the network to manage translations collectively.
    
- **Based on Site**:  
    Choose an existing site as a template. This copies content, settings, and configurations to save time.
    
- **Copy Attachments**:  
    Optionally copy media attachments from the source site to the new site.
    
- **Connect Content**:  
    If checked, all posts/pages from the source site are connected as translations on the new site.
    
- **Connect Comments**:  
    Synchronizes comments between the source post and its translations.
    
- **Plugins**:  
    Activates all plugins that are active on the source site for the new site.
    
- **Users**:  
    Copies users from the source site to the new site.
    
- **Search Engine Visibility**:  
    Optionally prevent search engines from indexing the new site.
    
- **Alternative Language Title**:  
    If enabled in Global Settings, set a custom title for the site that displays in the admin menu instead of the default title.
    
- **Redirect**:  
    If the Redirect module is active, configure automatic language redirection for this site and select if it should serve as a fallback.
    
    ![Settings - Add a new site](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/settings-add-a-new-site.png)
    

These options allow you to tailor how the new site integrates with your multilingual network.

---

## Step 4: Create the New Site

After configuring both the general and MultilingualPress-specific settings:

1. Click the button to **Add Site** or **Create Site**.
2. WordPress will create the new website, applying the settings you provided.
3. MultilingualPress links the new site with existing language sites, sets up relationships, and configures options like content connection and redirection as specified.

---

## Summary

By following these steps, you’ve successfully created a new language version of your site in your WordPress Multisite network using MultilingualPress. This process configures the site’s language, content relationships, redirection options, and more—ensuring it integrates smoothly into your multilingual setup.

**Next Steps**:

- Visit the newly created site’s dashboard to adjust site-specific settings if needed.
- Begin adding or translating content on the new site.
- Explore additional MultilingualPress guides for customizing language switchers, translating content, and managing modules.