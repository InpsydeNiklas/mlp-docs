Below are common terms, abbreviations, and concepts referenced throughout the MultilingualPress documentation and WordPress Multisite ecosystem. Use this glossary as a quick reference guide to clarify definitions and meanings.

---

# Glossary

## Block Editor (Gutenberg)

**Definition**: The modern, block-based editor introduced in WordPress 5.0.  
**Implication**: MLP 3+ is optimized for this editor, offering seamless translation metaboxes or blocks.

---

## Classic Editor

**Definition**: The older WordPress editing experience, pre-WordPress 5.0.  
**Usage**: Some site owners or enterprises continue using it for stability or plugin-compatibility. MultilingualPress remains fully compatible with it.

---

## CLI Commands

**Definition**: **WP-CLI** scripts for automating tasks within WordPress Multisite.  
**MLP Note**: MLP adds commands to link translations, copy media across subsites, or create new language sites programmatically.

---

## Domain

**Definition**: A unique address (like `example.com`) used to host a site.  
**In Multisite**: Each subsite can be in a subfolder (`example.com/fr`), subdomain (`fr.example.com`), or mapped to its own domain (`example.fr`).

---

## Domain Mapping

**Definition**: Assigning a custom domain (e.g., `example.fr`) to a Multisite subsite (e.g., `example.com/fr`).  
**Purpose**: Gives each language or regional site a unique domain, beneficial for branding and SEO.

---

## FSE (Full Site Editing)

**Definition**: An extension of the block editor enabling editing of entire site layouts (headers, footers, templates) via blocks.  
**Relation to MLP**: MLP supports block-based designs, ensuring multilingual sites remain compatible with FSE.

---

## Master API Key / Product ID

**Definition**: License credentials used to activate MLP or add-ons within a network.  
**Purpose**: Provides access to updates and support if you hold a valid subscription.

---

## MLP

**Stands For**: **MultilingualPress**  
**What It Is**: A plugin that creates multilingual functionality in WordPress by assigning each language version its own subsite.  
**Context**: Frequently referenced as MLP 3+ for the latest major version.

---

## Network Admin

**Definition**: The main administrative dashboard in a WordPress Multisite network.  
**Access**: Only a “Super Admin” manages all subsites, themes, and plugins from here.

---

## Page Builders (Elementor, Beaver Builder, etc.)

**Definition**: Third-party plugins offering drag-and-drop editing.  
**MLP Note**: MLP supports popular builders (e.g., Elementor, Beaver Builder, WPBakery, etc.), ensuring that builder-generated content can be translated or linked between subsites.

---

## Quick Sync / Copy Attachments

**Definition**: A MultilingualPress feature allowing images or media to be copied from one subsite to another, typically used in site duplication or content linking.  
**Context**: Minimizes manual uploads across multiple language sites.

---

## Quicklinks

**Definition**: A feature in MLP displaying inline language links within content.  
**Benefit**: Allows rapid navigation between language versions, without needing a separate menu widget.

---

## Source Site

**Definition**: In MLP, the site used as a template when duplicating settings, content, or plugin activations for creating a new language subsite.  
**Example**: The English site might serve as the “source” for creating a French site, replicating selected content and configurations.

---

## Subsite (Blog)

**Definition**: An individual website within a WordPress Multisite network.  
**Also Known As**: “child site” or “blog” in the database.  
**Example**: `example.com/es` if it’s a subdirectory, or `es.example.com` for a subdomain.

---

## Super Admin

**Definition**: The top-level admin role in a Multisite network.  
**Scope**: Can install plugins, activate themes network-wide, create or remove subsites, and assign users to sites globally.

---

## WooCommerce

**Definition**: The leading eCommerce plugin for WordPress.  
**Relation to MLP**: MLP integrates WooCommerce to create multilingual online stores. Each subsite can handle separate products, currencies, or shipping settings. Optional add-ons allow shared inventory or unified order data.

---

## WordPress Multisite

**Definition**: A WordPress core feature enabling multiple “subsites” under one installation. Each site can have distinct themes, plugins, and content.  
**Key Benefit**: Centralized management of updates, user roles, and plugin distribution—ideal for multilingual or multi-regional solutions.

---

**Last Updated**: _[Enter date or version]_

Keep this **Glossary** bookmarked as you navigate MLP’s documentation, so you can quickly interpret references to network admin, domain mapping, the block editor, or other terms in the WordPress multisite sphere!