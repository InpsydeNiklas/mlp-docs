# How to Automatically Forward Website Visitors to the Right Language Version with MultilingualPress

**Purpose**: Set up automatic redirection so visitors are taken to the language version of your site that matches their preferences, using the latest MultilingualPress redirection options.

---

## Overview

**Redirection** is an essential feature for multilingual websites, as it ensures that visitors are automatically taken to the language version of the site that matches their preferences (either through browser settings or geolocation). MultilingualPress makes it easy to set up automatic redirection, improving user experience by reducing the effort needed to switch languages manually. Recent updates provide additional flexibility in how redirection is executed and detected. This guide will walk you through activating and configuring these features.

---

## Steps to Set Up Automatic Language Redirection

### 1. Activate the Redirect Module

1. Navigate to **My Sites → Network Admin → MultilingualPress → Modules**.
2. Activate the **Redirect** module.

_Note_: The **Redirect** tab in global settings and additional redirection options become available only after this module is activated.

### 2. Configure Global Redirect Settings

After activating the Redirect module, go to the **Redirect** tab in MultilingualPress global settings. Here you can adjust new redirection options:

- **Redirect Fallback**:
    - Select a fallback network site URL where users are redirected if their preferred language doesn't match any available language sites.
    
- **Redirect Execution**:
    - Choose the programming method for redirection:
        - **Server-side redirect (PHP)**: Redirects visitors on the server before the page loads.
        - **Client-side redirect (JavaScript)**: Redirects visitors in the browser after the page loads.
        
- **Redirect Type**:
    - Choose the detection method and behavior for redirection:
        - **Browser language (Header)**: Detects the browser's language preferences.
        - **Geolocation (IP Address)**: Uses IP-based geolocation (via geoplugin or similar) to detect visitor location.
        - **Geolocation with fallback to browser language**: Attempts geolocation first, falling back to browser language detection if necessary.

Select settings that best suit your site's audience and technical environment. Save changes once configured.

### 3. Assign Languages to Your Sites

For each site in your network:

1. Go to **My Sites → Network Admin → Sites**.
2. Edit a site and, under the **MultilingualPress** tab, assign the correct language for that site (e.g., French, German).

### 4. Link Sites Together

- In **My Sites → Network Admin → Sites**, edit each site.
- Under the **MultilingualPress** tab, link sites by specifying relationships between language versions. This sets up the network of connected multilingual sites.

### 5. Link Content Across Sites

- While editing content on the source site, use the **MultilingualPress translation metaboxes** below the editor to link or create translations for corresponding posts/pages on connected sites.
- Ensure that content is correctly linked between language versions to enable effective redirection.

### 6. Verify Browser Language Settings

MultilingualPress uses visitor language settings for redirection. Check your browser’s language preferences to test redirection behavior. For example, in Google Chrome:

1. Go to **Settings → Languages**.
2. Adjust preferred languages as needed to simulate visitors from different locales.

![Browser language settings example](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/browser-language-settings.png)

---

## **Troubleshooting Common Issues** 

### **Problem: Redirection Not Working**
- **Solution**: Ensure that the **Redirect** module is activated and that language relationships between sites are correctly set up. Double-check the configuration of the redirect method (server-side or client-side).

### **Problem: Fallback Is Not Redirecting Correctly**
- **Solution**: Confirm that the fallback site URL is correctly set in the MultilingualPress settings and that the visitor’s preferred language is not mistakenly redirected to an unsupported language.

---

## Additional Considerations

- **Testing Redirection**: 
    - After setting up, simulate visitors with various browser languages or IP addresses to verify correct redirection behavior.

- **Fallback Behavior**: 
    - Ensure a fallback site is configured, so visitors with unsupported languages are directed appropriately.

- **Content Linking**: 
    - Proper linking of content across sites is crucial for smooth redirection. Verify that translations exist and are correctly connected.

---

## Summary

By activating the Redirect module, configuring fallback and execution options, assigning languages, linking sites, and connecting content, MultilingualPress will automatically forward visitors to the appropriate language version of your site. The new options for redirection execution and detection provide greater flexibility in tailoring the visitor experience to your needs.