---
title: Usage
parent: Post Publisher
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

Imported posts appear under the **wordable_import** post type in the sidebar (labeled based on your site). Each import has a **Build Layout** action link.

---

## Building a post

### Step 1: Open the builder

From the import list, click **Build Layout** next to the post you want to publish.

### Step 2: Configure settings

At the top of the builder page:

- **Builder** — Enfold or Elementor (auto-detected from your theme, but can be toggled)
- **Status** — Draft or Publish
- **Template** — A, B, or C (different layout structures)
- **Full-Width Header** — toggle for a wide header section
- **Sidebar** — add a sidebar to the layout
- **Featured Image** — select from the import's metadata or choose from media library
- **Categories** — multi-select which categories to assign

### Step 3: Review content

The builder shows the imported content organized into sections. You can drag and drop content between sections.

### Step 4: Set SEO metadata

- **Meta Title** — pulled from the import, editable
- **Meta Description** — pulled from the import, editable
- Saved to Yoast SEO fields on the published post

### Step 5: Save

Click **Save** to:
1. Create a new `post` with the builder layout
2. Set featured image, categories, and Yoast metadata
3. Trash the original `wordable_import`
4. Redirect to the new post's editor

---

## Templates

### Template A
Standard blog layout — full-width header, content in a single column.

### Template B
Two-column layout with content and sidebar sections.

### Template C
Multi-section layout with alternating column widths (66/34, 34/66 splits).

---

## Header options

Headers can use:
- **Image background** — from the featured image or a custom attachment
- **Video background** — embed URL
- **Solid color** — with optional overlay
- **Full-width or boxed** layout

---

## What happens to the import

After saving, the original `wordable_import` post is moved to WordPress trash. You can restore it from the trash if needed.
