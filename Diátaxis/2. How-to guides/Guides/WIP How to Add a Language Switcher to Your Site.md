**Purpose**: Learn about the various methods available in MultilingualPress 4 for adding a language switcher or navigation menu to your multilingual WordPress site. This guide provides a brief overview of each option, helping you choose the method that best fits your theme, technical skill level, and customization needs.

---

## Available Options for Adding a Language Switcher

MultilingualPress 4 offers multiple ways to display a language switcher:

### 1. MultilingualPress Language Block (Gutenberg)

- **What It Is**: A Gutenberg block that can be inserted anywhere within the WordPress editor where blocks are supported.
- **Advantages**:
    - Flexible placement within pages, posts, or template areas.
    - Seamlessly integrates with block-based themes and the new WordPress site editor.
    - Easily styled with CSS or adjusted using block settings.
- **Usage**:
    - Add the **Language Menu block** to your content to display a switcher.
    - [How to Set and Use the MultilingualPress Block Menu](#) – Detailed setup guide.

### 2. Language Switcher Widget (Legacy)

- **What It Is**: A widget for themes that support legacy (non-block) widgets.
- **Advantages**:
    - Quick to add to sidebars, footers, or other widget areas without modifying page content.
    - Provides basic customization options.
- **Usage**:
    - Activate the widget through **Appearance → Widgets** and configure settings.
    - [How to Set Up a Language Switcher for Multilingual WordPress Websites](#) – Detailed instructions for legacy widget configuration.

### 3. Language Navigation Menu

- **What It Is**: A standard WordPress navigation menu containing language links.
- **Advantages**:
    - Integrates language switcher into your site’s main navigation.
    - Managed through the familiar **Appearance → Menus** interface.
- **Usage**:
    - Create a language-based menu on one site, then copy it across others.
    - Refer to documentation on creating and copying language navigation menus.

### 4. Quicklinks

- **What It Is**: A feature that displays stylized language links directly within post content.
- **Advantages**:
    - Minimal setup, automatically injected into content based on available translations.
    - Provides an alternative style of language switcher without manual placement.
- **Usage**:
    - Enable Quicklinks in MultilingualPress settings to automatically display links.
    - Customize appearance with CSS for a distinct look.

### 5. Custom Language Switcher (Programmatic)

- **What It Is**: A fully custom language switcher built with code using MultilingualPress APIs.
- **Advantages**:
    - Complete control over markup, styling, and behavior.
    - Can integrate advanced logic like browser detection, geolocation, or custom design elements.
- **Usage**:
    - Write a custom plugin or theme code to generate language links using MultilingualPress hooks.
    - [How to Create a Custom Language Switcher in MultilingualPress](#) – Comprehensive guide.

---

## Choosing the Right Option

- **Modern, Block-Based Themes**: The **MultilingualPress Language Block** is generally recommended for its flexibility and integration with the Gutenberg editor.
- **Legacy Themes**: Use the **Language Switcher Widget** for simple integration in classic widget areas.
- **Navigation Integration**: If you prefer language links as part of your main menu, create a **Language Navigation Menu**.
- **Inline Links**: Use **Quicklinks** for automatic, styled language links embedded within content.
- **Advanced Customization**: For full control over appearance and behavior, build a **Custom Language Switcher** programmatically.


Each method can be further customized using CSS, JavaScript, and additional MultilingualPress settings. Depending on your theme and needs, select the option that offers the right balance of ease of use, flexibility, and control for adding a language switcher to your site.

For detailed steps on configuring any of these options, refer to the dedicated How-To guides linked above.