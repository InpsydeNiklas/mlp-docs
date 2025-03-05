# Domain Mapping with WordPress Multisite

**Purpose**: This document explains _what_ domain mapping is in the context of WordPress Multisite and _why_ it matters. While domain mapping once required a separate plugin, it became a native WordPress feature starting in version 4.5. By mapping individual domains (or subdomains) to subsites, you can maintain a clean URL structure—such as `example.fr`, `example.de`, or `store.example.com`—instead of the default `example.com/site2/` or `site2.example.com`.

---

## What Is Domain Mapping?

In a **WordPress Multisite** installation, all subsites by default share the main site’s domain but can use subfolders or subdomains for each subsite. For instance:

- **Subdirectory example**:
    - Main site: `my-network.com`
    - Subsite 1: `my-network.com/site1`
    - Subsite 2: `my-network.com/site2`
- **Subdomain example**:
    - Main site: `my-network.com`
    - Subsite 1: `site1.my-network.com`
    - Subsite 2: `site2.my-network.com`

Domain mapping replaces these default addresses with unique domains (e.g., `site1.com`, `site2.org`). This is beneficial for branding, language-based sites, or any scenario where each site requires its own top-level domain or subdomain.

---

## Why Map Domains to Subsites?

1. **Branding Consistency**  
    Each subsite can appear under a distinct domain, making them look like independent websites rather than subfolders or subdomains.
    
2. **Multilingual Websites**  
    If you’re hosting sites in multiple languages, you may prefer country-specific TLDs (e.g., `example.fr`, `example.de`) instead of `example.com/fr`.
    
3. **Easier External Linking**  
    Separate domains can simplify SEO and user recognition when each subsite stands alone in search results or marketing campaigns.
    
4. **No Extra Plugins Required**  
    Prior to WordPress 4.5, a dedicated plugin was needed to map custom domains to subsites. For a while now WordPress natively supports it, reducing overhead and complexity.
---

## Key Concepts

- **DNS (Domain Name System)**:  
    Ties your custom domain to the IP address or hosting server of your multisite. You must configure DNS records (A, CNAME, AAAA, Nameservers) so your domain points to the same server hosting your Multisite.

- **Hosting Dashboard**:  
    Depending on your hosting environment, you typically need to register each domain/subdomain in your hosting control panel (e.g., cPanel, Plesk) as an alias or parked domain. This step ensures the server knows to route domain requests to your WordPress Multisite.

- **Network Admin**:  
    In **My Sites → Network Admin → Sites**, you can edit each subsite to specify the **Site Address (URL)** as the new custom domain.

![[Pasted image 20250222233822.png]]

---

## How Domain Mapping Works in Practice

1. **WordPress Multisite Setup**  
    Begin by installing and configuring a WordPress Multisite with either subfolders or subdomains as the default structure.

2. **DNS Configuration**
    
    - Create the necessary DNS records so your custom domain (e.g., `my-new-site.com`) points to your hosting provider’s nameservers or IP address.
    - If using wildcards (e.g., `*.example.com`), you can map multiple subdomains without creating individual DNS entries each time.

3. **Host/Server Configuration**
    
    - In your hosting control panel, add the custom domain as an alias, parked domain, or additional domain.
    - This step ensures the server recognizes incoming requests for `my-new-site.com` and serves content from your multisite.

4. **Mapping the Domain in WordPress**
    
    - Go to **Network Admin → Sites**.
    - Click **Edit** for the subsite you want to map.
    - In **Site Address (URL)**, replace `site1.my-network.com` (or similar) with the custom domain `my-new-site.com`.
    - Save changes. Now WordPress will serve that subsite at the new domain.

5. **SSL Certificates**
    
    - For secure connections, each mapped domain typically needs its own SSL certificate (e.g., via Let’s Encrypt).
    - Proper SSL setup ensures HTTPS functions correctly across all mapped domains.

---

## Subdomains vs. Domain Mapping vs. Path-Based

- **Path-Based (Subfolders)**: E.g., `example.com/fr/`, suitable if you don’t mind showing a subfolder structure.
- **Subdomain**: E.g., `fr.example.com`, which can be combined with wildcard DNS for easier scaling.
- **Domain Mapping**: E.g., `example.fr` or `example-fr.com`, offering a completely distinct domain for each subsite.

**Mapping** transforms a default subfolder/subdomain subsite into a unique domain. This approach is common for brand or region-based sites, especially if the domain is already recognized by users.

---

## Common Use Cases

- **Multilingual Networks**: Each language site has a ccTLD (e.g., `example.es`, `example.de`).
- **Franchise Sites**: Each franchise subsite has a location-specific domain like `store-berlin.com`, `store-munich.com`.
- **Agency or Enterprise**: Multiple clients or departments each on their own domain, but centrally managed in one WordPress Multisite installation.

---

## Important Considerations

1. **DNS Propagation**  
    Changes to DNS records may take 24–48 hours to propagate globally.
    
2. **SSL for Each Domain**  
    If HTTPS is required, ensure a valid SSL certificate is installed and configured for each domain.
    
3. **Performance & Hosting Limits**  
    Depending on your host’s plan, domain mapping can introduce additional overhead—though typically far less than running multiple separate WordPress installs.
    
4. **Subsite URL Updates**  
    If you already have an established subsite, changing its URL to a mapped domain can affect existing internal or external links. Consider using redirects or updating references if needed.

---

## Conclusion

Domain mapping in WordPress Multisite allows each subsite to appear under its own domain—improving branding, user experience, and SEO. With WordPress 4.5 and later, this capability is natively integrated, reducing the need for third-party plugins. The general steps are:

1. **Set up Multisite** with subfolders or subdomains by default.
2. **Update DNS** so your custom domain points to the server hosting the multisite.
3. **Add the domain** to your hosting environment, typically as an alias or parked domain.
4. **Edit the subsite’s Site Address (URL)** in **Network Admin** to map the domain.
5. **Confirm SSL** if desired for secure browsing.

By managing all subsites in one network and leveraging domain mapping, you maintain a clean, cohesive system that can handle multiple languages, brands, or regions—all through the power of WordPress Multisite.