# How to Copy a Navigation Menu Across Multisite Sites with MultilingualPress

**Purpose**: Learn how to easily copy a navigation menu from one site to others in your WordPress Multisite network using MultilingualPress. This guide applies to traditional (non-block) themes where menus are managed via the classic Appearance → Menus interface.

---

## Overview

Creating and maintaining navigation menus on multiple sites can be time-consuming. MultilingualPress simplifies this by allowing you to create a menu once on a primary site and then copy it to other connected language sites, ensuring consistency and saving time. This process improves user experience by ensuring that the same navigation structure is applied across all language versions of the site.

---

## Steps to Copy a Navigation Menu

### 1. Create and Save a Language Menu on the Primary Site

1. On your **primary site** (e.g., English version), go to **Appearance → Menus** in the WordPress Dashboard.
    
2. Create a new menu:
    
    - Enter a **Menu Name** (e.g., "Main Menu").
    - Open the **Languages** section in the menu editor sidebar.
    - Select the checkboxes for all languages you want to include (e.g., English, Italian, German).
    
3. Click **Add to Menu** and then **Save Menu**.
    
    ![Setting languages menu in the English site](https://multilingualpress.org/wp-content/uploads/sites/12/2021/04/SettingMenu.png)
    
4. Verify the menu appears on the front end of the primary site with language options.
    
    ![English Site - Navigation Menu](https://multilingualpress.org/wp-content/uploads/sites/12/2021/04/EnglishVersionNavUpdated.png)

---

### 2. Copy the Menu to Other Sites

Although the primary site now displays the language menu, other language sites (e.g., Italian, German) may still show outdated menus.

1. On one of the target sites (e.g., the Italian site), go to **Appearance → Menus**.
    
2. Look for a dropdown menu created by MultilingualPress—this lets you select a menu configuration from another site.
    
    ![MultilingualPress - Copy Menu feature](https://multilingualpress.org/wp-content/uploads/sites/12/2021/04/CopyMenuMultilingualPress.png)
    
3. In the dropdown, select the **"main - Primary Menu"** from the primary (English) site.
    
4. Click the **Copy** button to import the menu configuration.
    
5. Repeat these steps on the **German site** or any other target site to copy the menu from the primary site.

---

### 3. Verify the Copied Menus

After copying:

- Navigate to the front end of each site to confirm that the navigation menu has been successfully updated with language links.
- The language menu should now be consistent across all connected sites with just a few clicks.

---

## Troubleshooting Common Issues *(New Addition)*

### **Problem: The Copied Menu Doesn’t Appear on the Target Site**
- **Solution**: Ensure that the correct **language relationship** is set up between the primary and target sites. Confirm that **MultilingualPress** is properly activated on both sites and that menu synchronization is enabled.

### **Problem: Menu Items Are Not Appearing Correctly**
- **Solution**: Check if the **language versions** of the menu items are correctly linked. Make sure that the menu items on the primary site are properly translated or created on the target sites.

---

## Important Notes

- **Legacy Themes**:  
    This menu copying feature is designed for traditional non-block themes that utilize the standard WordPress menu system.
    
- **Block Themes**:  
    For block-based themes, consider using the **MultilingualPress Language Menu Block** instead, which seamlessly integrates with the WordPress editor and replaces the need for legacy menu copying. This method provides more flexibility and is easier to manage within block-based themes.
    
- **Limitations**:  
    This guide focuses solely on copying navigation menus using MultilingualPress for legacy themes. It does not cover block theme implementations or advanced language switcher options. For users with complex menu structures (e.g., custom post types or advanced customization), further adjustments may be necessary.

---

By following this guide, you can efficiently propagate a consistent navigation menu across your multilingual sites, reducing repetitive work and ensuring a unified user experience.
