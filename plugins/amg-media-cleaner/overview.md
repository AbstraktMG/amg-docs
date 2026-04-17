---
title: Overview
parent: Media Cleaner
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG Media Cleaner finds and removes unused media files clogging your uploads folder. It scans your entire site — posts, meta, options, theme settings — to identify what's actually referenced, then flags everything else.

## What it does

- Scans for **unused attachments** — media not referenced anywhere on the site
- Finds **orphaned files** — files on disk with no database record
- Detects **broken attachments** — database records with missing files
- Flags **probably unused** — recently uploaded (< 90 days) media not yet referenced
- Supports **trash before delete** — review before permanent removal
- **Export CSV** for auditing before cleanup

## Categories

| Category | Meaning |
|----------|---------|
| Unused | No references found, uploaded over 90 days ago |
| Probably Unused | No references found, uploaded within 90 days |
| Orphaned | File exists on disk but no attachment record in database |
| Broken | Attachment record exists but file is missing from disk |

## What counts as "used"

The scanner checks everywhere:
- Post content (all post types)
- Featured images
- Post meta / custom fields
- WordPress options table
- WooCommerce product galleries
- Site icon and custom logo
- User avatars
- Gutenberg block references
