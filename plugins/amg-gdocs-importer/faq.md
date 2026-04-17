---
title: FAQ
parent: GDocs Importer
grand_parent: Plugins
nav_order: 4
---

# FAQ

### Why can't I see any documents?
The service account must be **shared** on the Google Drive folder. Share the folder with the `client_email` from your service account JSON.

### What post type does it create?
`wordable_import` — a draft post type used by AMG Publisher to build final blog layouts.

### Can I import directly as a regular post?
Not currently. The plugin creates `wordable_import` drafts, which you then process through AMG Publisher.

### Will it duplicate documents?
No. The plugin tracks which Google Doc IDs have been imported and flags them in search results. You'll see an "Already imported" label.

### Why does Test Connection fail?
Common causes:
- Service account JSON is invalid (check formatting)
- Google Drive/Docs APIs not enabled in Cloud Console
- Folder not shared with the service account email
- Folder ID is wrong

### Does it work with shared drives (Team Drives)?
It should work if the service account has access. Use the folder ID from the shared drive URL.

### How big can documents be?
The Google Docs API handles large documents, but very long docs (50+ pages) may take longer to process. Image-heavy docs are slower because each image is downloaded individually.

### Where do the images go?
Into the WordPress media library, uploaded under the current month's folder in `wp-content/uploads/`. URLs in the post content are rewritten to point to the local copies.

### Is my service account key secure?
Yes. If entered via the Settings UI, it's encrypted with AES-256-CBC using your site's auth salt before storage. If using Remote Config, it's encrypted the same way in the central config cache.
