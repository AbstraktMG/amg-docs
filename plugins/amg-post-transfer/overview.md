---
title: Overview
parent: Post Migration
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG Post Migration moves posts (and pages, custom post types, products, etc.) between WordPress sites. It packages the content, images, categories, tags, and custom fields into a single ZIP file you can upload on another site.

## What it does

Use it for things like:

- Moving a blog post from a staging site to a live site
- Cloning a set of pages to a new client website
- Backing up a small group of posts before a big change
- Sending content to a freelancer who works on a different site

It's **not a full site backup** — it's a precise tool for moving **specific posts** between sites.

## When to use it

| Situation | Use Post Migration? |
|-----------|----------------------|
| Moving 5–500 posts from Site A to Site B | Yes |
| Migrating a single landing page with images | Yes |
| Cloning content into a brand-new client site | Yes |
| Full site migration (theme, plugins, settings) | No — use a full migration tool |
| Backing up your entire database | No — use a backup plugin |
| Syncing content automatically on a schedule | No — this is a manual one-time tool |

## What gets transferred

**Included:**
- Post title, content, excerpt
- Featured image
- Categories, tags, and custom taxonomies
- Custom fields (ACF and standard meta)
- Author (remapped on import)
- Publish date and status
- Page builder content (Enfold, Elementor, Gutenberg, etc.)
- All media files referenced in the content (when "Bundle media" is selected)

**Not included:**
- Comments
- Theme settings
- Widget configuration
- Menus
- Plugin settings
- User accounts
- Site-wide options
