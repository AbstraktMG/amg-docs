---
title: FAQ
parent: Post Migration
grand_parent: Plugins
nav_order: 4
---

# FAQ

### What does this plugin do?
It moves posts and pages between WordPress sites by packaging them into a ZIP file you can download and upload elsewhere.

### Does it move my whole site?
No. It only moves the specific posts you select. Themes, plugins, settings, menus, and widgets are not included.

### Will my images come along?
Yes, if you choose **"Bundle media in ZIP"** during export. If you choose "Leave URLs," the new site will try to download images from the original location instead.

### What if the same post already exists on the destination site?
You choose during import:
- **Skip** — leave the existing post alone (safest)
- **Update** — overwrite it with the imported version
- **Import as new** — create a duplicate with a different slug

### Can I undo an import?
No. There's no built-in undo. Always test on a staging site first, and use "Skip duplicates" when in doubt.

### Why is my export ZIP so big?
Bundled media (images, PDFs, videos) makes ZIPs large. If it's over your hosting upload limit, export in smaller batches or use "Leave URLs" instead.

### My import says "0 posts imported." Why?
Most common cause: you chose "Skip duplicates" and every post in the ZIP already exists on the destination. Try "Update" or "Import as new."

### Do custom fields (ACF) come along?
Yes — but the field definitions need to exist on the destination site. Make sure ACF is installed and your field groups are set up before importing.

### Will my Elementor layouts work after import?
Yes. The importer rewrites image URLs, attachment IDs, and preserves JSON escaping so Elementor layouts render correctly on the destination. Clear Elementor's CSS cache after import (Elementor → Tools → Regenerate CSS).

### Will my Enfold layouts work after import?
Mostly yes. If page builder layouts look broken (especially images), run **AMG Post Repairer** afterward to fix shortcode ID references.

### Can I import pages as a different post type?
Yes. During import, use the Post Type Mapping section to switch any source type (e.g., `page`) to any other registered post type on the destination (e.g., `case_study`).

### Can two people export at the same time?
Yes. Each export gets a unique ID, so they don't interfere.

### How big a batch can I import?
Technically unlimited, but for slow hosting, stick to ~100 posts per batch to avoid timeouts.

### Where do exported ZIPs go?
They download directly to your computer (Downloads folder). They're not stored on the site.

### Is this safe to use on a live client site?
For exports — yes, completely. For imports — always test on staging first, especially if using "Update duplicates."

### What's the difference between this and a backup?
Backups capture your entire site (database + files + settings). Post Migration moves specific content between sites. They're different tools for different jobs.
