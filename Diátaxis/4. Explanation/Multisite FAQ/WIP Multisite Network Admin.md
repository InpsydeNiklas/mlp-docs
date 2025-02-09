# Multisite Network Admin

**Purpose:**  
This document provides an overview of the **Multisite Network Admin** area in WordPress Multisite, explaining user roles, the structure of the network administration interface, and key functions available to Super Admins. It serves as a guide to understanding how centralized management simplifies user and site administration across a network of interconnected sites.

---

## User Roles in WordPress Multisite

In a Multisite environment, user capabilities are structured into distinct roles:

- **Super Admin**:
    - Holds the highest level of control across the entire network.
    - Can install and manage plugins/themes, create or delete subsites, manage users across all sites, and configure network-wide settings.
    - The only user who can access the **Network Admin** dashboard.
- **Site Administrator**:
    - Manages content, pages, posts, and site-specific settings on individual subsites.
    - Cannot install plugins or themes; can only activate ones that the Super Admin has made available.
    - Lacks access to network-level settings and the overall administration of other sites.
- **Other WordPress Roles**:
    - Subscriber, Contributor, Author, Editor: These roles exist on each subsite, with standard capabilities limited to that particular site’s content management, unless extended by network policies.

---

## What Is the Network Admin Area?

The **Network Admin** dashboard is a special control panel accessible only to Super Admins. It provides centralized tools to manage the entire multisite network from any subsite’s admin area. Key characteristics include:

- **Centralized Management**:
    - Manage all subsites, users, themes, plugins, and network settings in one place.
    - Single sign-on allows seamless navigation between sites without re-authentication.
    - <!-- Note: Add a screenshot of the Network Admin dashboard here to help visualize the centralized management process. -->
- **Simplified User Management**:
    - Users added at the network level are registered across all subsites, with roles assigned per site.
    - Network registration settings control how users can register and create new sites within the network.

---

## Key Sections of the Network Admin Dashboard

### Dashboard

- **Home**: Quick links for creating new sites, managing users, and checking for updates.
    - Summaries of network activity, such as recent site creations or WooCommerce orders.
    - <!-- Note: Add a screenshot here of the Network Admin dashboard with quick links highlighted. -->
- **Updates**:
    - Oversee and apply updates to WordPress core, themes, and plugins across the network.
    - Upgrade all sites in the network after a WordPress core update to ensure consistency.

### Sites

- **Site Management**:
    - View a list of all subsites.
    - Access options to edit site settings, switch to a subsite’s dashboard, activate or deactivate, archive, mark as spam, or delete subsites.
    - Add new sites with designated titles, URLs, languages, and admin users.

### Users

- **Network-Wide User Administration**:
    - Add or manage users across the entire network.
    - Assign users to specific subsites or update roles.

### Themes & Plugins

- **Central Resource Management**:
    - Install and update themes and plugins at the network level.
    - Network activate themes/plugins to make them available or active across all sites.
    - Site administrators can activate network-enabled themes or plugins locally, subject to restrictions set by the Super Admin.

### Settings

- **Global Settings Configuration**:
    - Control defaults like user registration policies, theme/plugin availability for site admins, and other network behaviors.

---

## Benefits of the Network Admin Area

- **Centralization**: Super Admins can monitor and manage all aspects of the network without navigating between separate installations.
- **Efficiency**: Streamlines tasks like installing plugins or activating themes across multiple sites at once.
- **User Control**: Simplifies global user management, enabling single sign-on and consistent role assignments across subsites.
- **Scalability**: As networks grow to include many sites, the Network Admin area provides tools to handle extensive lists of subsites, large user databases, and numerous themes/plugins.

---

## Summary

The **Multisite Network Admin** is the heart of a WordPress Multisite installation. It empowers Super Admins to efficiently manage an entire network of sites from one centralized dashboard while maintaining distinct administration layers for individual site administrators. Understanding the roles, layout, and capabilities of Network Admin is crucial for effectively operating and scaling a multisite network, particularly for multilingual projects leveraging plugins like MultilingualPress.

## Helpful Resources

- [Managing a WordPress multisite network (Video)](https://learn.wordpress.org/lesson/managing-a-wordpress-multisite-network/)
- [Advanced multisite management (Video)](https://learn.wordpress.org/lesson/advanced-multisite-management/)
