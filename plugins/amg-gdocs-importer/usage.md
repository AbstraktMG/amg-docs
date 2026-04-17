---
title: Usage
parent: GDocs Importer
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

**AMG → GDocs Importer**

Two tabs: **Import** and **Settings**.

---

## Import tab

### Searching for documents

1. Type a document title (or part of it) in the search box
2. Click **Search** or press Enter
3. Results show: document title, owner, last modified date
4. Already-imported docs are flagged to prevent duplicates

### Importing a single document

1. Find the doc in search results
2. Click **Import**
3. The plugin:
   - Fetches the Google Doc content via the Docs API
   - Converts formatting to Gutenberg blocks (headings, paragraphs, lists)
   - Downloads images from the doc into WordPress media library
   - Creates a `wordable_import` draft post
4. A success message appears with a link to the new post

### Batch importing

1. Search for documents
2. Select multiple docs using the checkboxes
3. Click **Import Selected**
4. A progress bar shows each doc being processed
5. Results log shows which docs were imported, skipped, or failed

### What gets imported

- Headings (H1–H6)
- Paragraphs
- Bullet and numbered lists
- Images (downloaded from Google, saved to media library)
- Bold, italic, and link formatting
- Tables (basic support)

### What doesn't get imported

- Comments and suggestions
- Footnotes
- Drawing objects
- Headers/footers
- Custom fonts (converted to default theme font)

---

## Settings tab

- **Service Account JSON** — paste your Google service account key (if not using Remote Config)
- **Google Drive Folder ID** — the folder to search within
- **Test Connection** — verifies the credentials work and the folder is accessible
