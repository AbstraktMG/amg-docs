---
title: Usage
parent: Post Repairer
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

**AMG → Post Repairer**

---

## Workflow

### Step 1: Configure settings

Expand the settings panel and set your target builder, post types, colors, and source URL. Click **Save Settings**.

### Step 2: Scan posts

1. Select posts using checkboxes (or Select All)
2. Choose **Scan only** from the Bulk Actions dropdown
3. Click **Apply**
4. Each post gets a builder badge showing what created it (Enfold, Elementor, Gutenberg, etc.)

### Step 3: Convert

1. Select the scanned posts you want to convert
2. Choose **Convert only** from Bulk Actions
3. Click **Apply**
4. The plugin:
   - Creates a backup of the original content
   - Converts to the target builder format
   - Updates post content and builder-specific metadata
   - Shows a status badge (Complete or Error)

### Step 4: Repair (optional)

After conversion, you may need additional repairs:

- **Repair Images** — fixes broken attachment IDs, attempts to download missing images from the source URL, falls back to placeholder
- **Repair Colors & Sidebar** — applies heading/body colors and sidebar layout to Enfold posts

Or use **All (Scan → Convert → Repair)** to run everything in one pass.

---

## Available actions

| Action | What it does |
|--------|--------------|
| All | Scan + Convert + Repair Images + Repair Colors in sequence |
| Scan only | Detect the page builder for each post |
| Convert only | Convert content to the target builder |
| Repair Images only | Fix broken image references |
| Repair Colors & Sidebar only | Apply color/sidebar settings (Enfold only) |
| Restore from backup | Revert to the original pre-conversion content |

---

## Post table columns

- **Thumbnail** — current featured image
- **Title** — post title (links to editor)
- **Post Type** — post, page, or CPT
- **Builder** — detected page builder (after scan)
- **Status** — Pending, Complete, or Error
- **Image Status** — number of images fixed/missing
- **Actions** — per-row action buttons

---

## Restoring from backup

Every conversion creates a backup. To restore:

1. Select posts with the 💾 backup indicator
2. Choose **Restore from backup** from Bulk Actions
3. Click **Apply**
4. Original content is restored, conversion metadata cleared
