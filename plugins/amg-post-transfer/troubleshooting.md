---
title: Troubleshooting
parent: Post Migration
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| Images broken after import | Used "Leave URLs" but source site is offline | Re-export with "Bundle media" |
| Elementor layouts look flat / one text block | Older plugin version (pre-beta.12) corrupted JSON escaping on save | Update to latest, delete the imported post, re-import |
| Imported page at `/case-studies/` shows CPT archive instead | A CPT with `has_archive => true` and `rewrite slug` matching the page slug | Change the CPT's rewrite slug or disable its archive |
| "No posts imported" / zero results | "Skip duplicates" active + slug exists on destination (including trashed!) | Empty trash for that post type, try "Update" or "Import as new" |
| Upload times out | ZIP is too big for hosting upload limit | Export in smaller batches, or increase `upload_max_filesize` |
| Layout broken on Enfold pages | Builder shortcodes reference IDs from old site | Run **AMG Post Repairer** after import |
| Custom fields missing | ACF / custom field plugin not active on destination | Activate the plugin, then re-import |
| Internal links still point to source domain | Only media URLs are remapped automatically; page links are not | Run a DB search-replace for the source domain on the destination |

## Do's and don'ts

### ✅ Do
- **Always test on staging first** when importing onto a live client site
- **Bundle media in ZIPs** unless file size is a problem
- **Use "Skip duplicates"** the first time you run an import — safer than overwriting
- **Note the source site** before exporting (stored in the ZIP, but good to confirm)
- **Check the preview** carefully — post counts, types, and media counts should match what you expected

### ❌ Don't
- **Don't import the same ZIP twice with "Update duplicates"** — you'll wipe any local edits
- **Don't expect theme settings, widgets, or menus to come along** — only post content transfers
- **Don't try to import 1,000 posts in one shot** if your hosting is slow — break into batches of ~100

## If Elementor pages still look wrong after import

1. Go to **Elementor → Tools → Regenerate CSS & Data** (or "Clear Files & Data")
2. Open one imported post with **Edit with Elementor** and click Update to force CSS regeneration
3. Verify the destination theme supports Elementor for that post type (Elementor → Settings → General → Post Types)
4. Check the browser console for missing asset errors — clear any CDN/caching plugin cache
