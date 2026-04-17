---
title: Usage
parent: Media Cleaner
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

**AMG → Media Cleaner**

Two tabs: **Results** and **Trash**.

---

## Running a scan

1. Click **Scan Now**
2. A progress bar shows each phase:
   - Quick ID lookups (featured images, gallery, site icon)
   - Post content scan
   - Post meta scan
   - Options table scan
   - Attachment comparison
   - Orphan file scan
3. When complete, results appear in the table below

If a scan stalls (no progress for 5+ minutes), a **Resume Scan** button appears.

## Reading results

Summary badges at the top show counts and total file size per category (color-coded).

The table shows each flagged file with:
- **Preview** — click for a lightbox view
- **File Path** — relative to uploads
- **Category** — Unused, Probably Unused, Orphaned, or Broken
- **Size** — disk space used
- **Uploaded** — when the file was added
- **Reason** — why it was flagged

Use the **category filter** and **search box** to narrow results.

---

## Deleting files

### Recommended workflow: Trash first

1. Select files using checkboxes (Shift+click for range selection)
2. Click **Trash Selected** — moves attachments to WordPress trash
3. Switch to the **Trash** tab to review
4. If everything looks right, click **Delete Permanently** on the Trash tab
5. Or click **Restore Selected** to put them back

### Direct permanent delete

From the Results tab, click **Delete Permanently** on selected items. A confirmation modal shows the count. This cannot be undone.

### Orphaned files

Orphaned files (no database record) can only be permanently deleted — they can't be trashed since they have no attachment record.

---

## Export CSV

Click **Export CSV** to download a spreadsheet of all scan results. Useful for auditing before cleanup or sharing with a client.

---

## Trash tab

Shows all WordPress trashed media (not just items flagged by Media Cleaner). You can:
- **Restore Selected** — move back to the media library
- **Delete Permanently** — remove from disk forever
