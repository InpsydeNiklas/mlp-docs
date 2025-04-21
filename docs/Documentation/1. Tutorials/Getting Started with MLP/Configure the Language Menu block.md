---
title: Configure the Language Menu block
nav_order: 6
parent: Tutorials
has_children: false
---


**Purpose**: Use the **Language Menu** block from MultilingualPress to let visitors switch between different language sites. You can insert it into individual posts/pages or place it site-wide using a Full Site Editing (FSE) theme. This guide covers activation, placement, and special considerations if you create a new site based on another.

---

### 1. Enable the “Gutenberg Blocks” Module

1. **Open Global Settings**
   - From the admin toolbar, go to:  
     **My Sites** → **Network Admin** → **MultilingualPress** → **Modules**.
2. **Activate Gutenberg Blocks**
   - Find **Gutenberg Blocks** in the **Modules** list.  
   - Check the box next to it and click **Save Changes**.

> **Tip:** If the **Gutenberg Blocks** module is not enabled, the **Language Menu** block will not appear in the editor.

![MultilingualPress Modules](https://multilingualpress.org/wp-content/uploads/sites/12/2022/10/image5.png)

Once saved, the **Language Menu** block is available in the WordPress editor.

---

### 2. Insert the Language Menu Block

#### 2.1. Add to a Post or Page

1. **Open the Editor**
    - Go to any post or page and click **Edit**.
2. **Add the Block**
    - In the Gutenberg editor, click the **+** icon or type `/` to open the block inserter.
    - Search for **MultilingualPress: Language Menu** and select it.

![Insert the Language Menu Block](https://multilingualpress.org/wp-content/uploads/sites/12/2022/10/image2.png)

3. **Configure Your Languages**
    - Select the **Language Menu** block to see its settings in the right sidebar.
    - Check the box for each language/site you want to include.
    - **Order**: The order in which you check them determines their display order. Deselect/reselect if needed.

![Select Languages in Sidebar](https://multilingualpress.org/wp-content/uploads/sites/12/2022/10/image3.png)

#### 2.2. Add to Site-Wide Areas (Full Site Editing Theme)

1. **Open the Site Editor**
    - Go to **Appearance → Editor** (available in block/FSE themes).
2. **Locate a Template or Template Part** (e.g., Header or Footer)
    - Access your templates and template parts via the WordPress icon in the top-left corner.
    - Select the **Header**, **Footer**, or any area where you’d like the switcher to appear.
3. **Insert the Block**
    - Click the **+** icon, search for **MultilingualPress: Language Menu**, and select it.
    - Configure languages as in Step 2.1.3.
4. **Save Your Changes**
    - Click **Save** to publish changes across your site.

#### 2.3. Add the Language Menu to a Newly Created Site

If you followed the [Create a new language version of the site](#create-new-language-site) tutorial and just created a new site using the **“Based on”** option in MultilingualPress, and the **source site** did **not** yet have the Language Menu block set up, you must manually add it to the new site:

1. **Switch to the New Site**
    - In the admin toolbar, hover over **My Sites** and select the newly created site’s **Dashboard**.
2. **Follow the Same Steps**
    - Enable the “Gutenberg Blocks” module if not already active (**MultilingualPress → Modules**).  
    - Add the **Language Menu** block to a page, post, or site-wide template in the new site, just like in Steps 2.1 or 2.2.
3. **Customize**
    - Adjust the languages and styling as needed.
    - Confirm the menu links correctly to the other multilingual sites in your network.

> **Note:** New sites created using the **“Based on Site”** option may not inherit all settings from the source site, including the **Language Menu block**. Ensure that the **Gutenberg Blocks** module is enabled and the block is added manually if needed.

---

### 3. Verify Your Language Switcher

- **Preview or Update** to see the Language Menu in action.  
- Click on a language in the switcher to confirm it takes you to the correct site.

If the switcher doesn’t appear, ensure **Gutenberg Blocks** is still active under **MultilingualPress** → **Modules**, and check you’ve saved any Site Editor template changes.

---

### 4. Next Steps

- **Customize Styles**: Use the WordPress block settings to adjust the menu’s alignment, text size, or colors.  
- **Troubleshoot**: If you still don’t see the switcher or need additional guidance, consult our [support team](https://multilingualpress.org/support/).
- **Continue**: [Publish New Content in Multiple Languages](#step6) to learn how to create and translate posts across your network.

By placing the Language Menu block in posts, pages, or site-wide areas, you empower visitors to navigate between different language versions of your content effortlessly.
