**Purpose**: Quickly replicate or bulk-copy media files (images, PDFs, etc.) from one subsite to another in a WordPress Multisite, using MultilingualPress (v4.6.0 or later).

---

## 1. Prerequisites

1. **WordPress Multisite** with at least two sites connected via MultilingualPress.
2. **MultilingualPress**: Version 4.6.0 or above.
3. **Media Files** in at least one site’s Media Library.

---

## 2. Copy a Single Media File

1. **Go to the Source Site’s Media Library**
    - For example, if the **English site** has an image you want to copy to the **German site**, go to **My Sites → [English Site] → Media**.
2. **Open the File Details**
    - Click on an image (e.g., a photo of Woody Allen) to view its attachment details.
3. **Scroll to “MultilingualPress Setting”**
    - On the right-hand side, find the “MultilingualPress Setting” section.
    - Choose **one or more** connected sites to which you want to copy the file.
4. **Click “Copy”** (or equivalent button)
    - The file is immediately copied to the selected site(s).
    - **Note**: If a file with the same name exists on the destination site, it will be **overwritten**.

**Verification**:

- Switch to the destination site (e.g., **My Sites → [German Site] → Media**).
- Confirm the newly copied file appears in the Media Library.

---

## 3. Copy Multiple Media Files in Bulk

1. **Open the Source Site’s Media Library**
    - Example: You have multiple images in the **Italian site** that you want to copy to the **German site**.
2. **Click “Bulk Select”**
    - A new section appears, letting you choose the **destination site(s)** for the bulk copy operation.
3. **Select Destination Site(s)**
    - In the MultilingualPress panel, check the box for each site to which you want to copy the files.
4. **Select the Files**
    - Click each file (or “Select All”) you want to copy.
5. **Press “Copy”**
    - MultilingualPress copies all selected media files to the chosen site(s).

**Verification**:

- Switch to the destination site’s Media Library.
- All selected images/files should now appear, ready for use.

---

## 4. Important Notes

- **Overwrites Existing Files**: If a destination site already has a file of the same name, it will be **replaced** with the new copy.
- **Consistency Across Languages**: Once copied, you can insert or reference these media files in posts/pages on the destination site without needing to manually upload them again.
- **Bulk vs. Single**: Use **Bulk Select** when you need to copy multiple files at once; for ad hoc or single-item transfers, copy individual files from their attachment details screen.

---

## Summary

With **MultilingualPress 4.6.0+**, you can seamlessly duplicate any media library items to one or more connected subsites, saving time and ensuring consistent branding or assets across your multilingual WordPress network.

- **Next Steps**:
    - Explore other advanced content syncing options in MultilingualPress.
    - Maintain consistent file naming to avoid unintended overwrites.

By following these steps, you’ll streamline media management across all your language sites—no more manual downloads and re-uploads for each subsite!