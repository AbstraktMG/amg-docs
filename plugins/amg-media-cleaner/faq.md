---
title: FAQ
parent: Media Cleaner
grand_parent: Plugins
nav_order: 4
---

# FAQ

### Is it safe to delete everything flagged as "Unused"?
Generally yes, but review first. The scanner checks post content, meta, options, and theme settings — but it can't detect media referenced in hardcoded theme templates or JavaScript. When in doubt, trash first and test the site before permanent deletion.

### What's the difference between "Unused" and "Probably Unused"?
**Probably Unused** means the file was uploaded within the last 90 days. It might be in use but not yet referenced (e.g., staged for a future post). Give it time before deleting.

### Will it delete my site icon or logo?
No. The scanner checks site icon, custom logo, and user avatars — these are always marked as "used."

### Does it work with page builders (Elementor, Enfold)?
Yes. The scanner checks post meta where page builders store image references. However, images referenced only in Elementor's cached CSS (not in `_elementor_data`) might be missed.

### Does it handle WooCommerce product galleries?
Yes. The `_product_image_gallery` meta is explicitly checked.

### Can I undo a permanent delete?
No. Once files are permanently deleted, they're gone. Always trash first and verify before permanent deletion.

### How long does a scan take?
Depends on site size. A small site (100 posts, 500 media) takes 1-2 minutes. A large site (5,000 posts, 10,000 media) takes 5-15 minutes. The scan runs in batches to avoid timeouts.

### What if a scan stalls?
Click **Resume Scan**. The scanner saves its position and can pick up where it left off. Stalls are detected after 5 minutes of no progress.

### Does it delete PHP files or .htaccess?
Never. Executable files (.php, .sh, .htaccess, etc.) are blocked from deletion regardless of orphan status.
