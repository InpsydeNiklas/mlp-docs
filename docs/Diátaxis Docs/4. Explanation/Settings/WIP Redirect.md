## Redirect Settings in MultilingualPress

**Overview**:  
The **Redirect** tab in MultilingualPress global settings becomes available only when the Redirect module is activated under the **Modules** tab. This tab provides options to manage automatic language redirection across your Multisite network, ensuring visitors are directed to the appropriate language version of your content.

![MultilingualPress Redirect Settings](https://multilingualpress.org/wp-content/uploads/sites/12/2018/07/Redirect.png)

### Key Options in the Redirect Tab

- **Redirect Fallback**:
    
    - **Purpose**: Specifies a network site to serve as a fallback destination if a visitor's preferred language isn't available on any connected site.
    - **Use Case**: Direct users to a default language site when no matching language content is found.
- **Redirect Execution**:
    
    - **Purpose**: Selects the programming method (PHP or JavaScript) used for performing the redirection.
    - **Considerations**:
        - **PHP-based redirects** execute server-side and often provide faster user experiences but may require additional server resources.
        - **JavaScript-based redirects** execute in the browser, offering flexibility but potentially slower performance if scripts fail to load.
- **Redirect Type**:
    
    - **Purpose**: Determines the logic for how redirection should occur, based on different detection methods.
    - **Options**:
        1. **Browser language (Header)**:
            - Detects the user's browser language preferences and redirects them to the corresponding country site if it exists.
            - Falls back to the specified fallback site if the desired language isn’t available.
        2. **Geolocation (IP Address)**:
            - Uses the visitor's IP address and the [geoplugin](https://www.geoplugin.com/) service to detect their country.
            - Redirects to the corresponding country site if available; otherwise, to the fallback site.
        3. **Geolocation with fallback to browser language**:
            - First attempts geolocation-based redirection using the IP address.
            - If no appropriate site exists, it defaults to detecting the browser language as in the first option.

### How It Works

When enabled, the Redirect module creates a new **Redirection** tab in the global settings. This tab allows administrators to:

- Designate a fallback site.
- Choose redirection execution methods and types.
- Manage per-site redirection preferences in each subsite’s MultilingualPress settings, including options for automatic redirection and fallback designations.

By configuring these options, administrators can ensure that visitors are seamlessly redirected to the best available language version of a page, enhancing user experience and localization effectiveness.