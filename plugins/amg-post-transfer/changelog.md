---
title: Changelog
parent: Post Migration
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 1.0.0-beta.13 — Apr 10, 2026
- Debug cleanup and final stability pass

## 1.0.0-beta.12 — Apr 10, 2026
- **Fix:** `_elementor_data` JSON corruption on import (the root cause of missing layouts). `update_post_meta` calls `wp_unslash`, stripping backslashes that Elementor needs for escaped quotes and slashes. Now wraps in `wp_slash()` before saving.
- All Elementor pages now import with correct containers, layouts, and background images

## 1.0.0-beta.11 — Apr 9, 2026
- Attempt at escaped-slash URL mapping for `_elementor_data` (superseded by beta.12)

## 1.0.0-beta.10 — Apr 9, 2026
- Added `remap_builder_urls_by_filename()` for foreign-domain image URLs in builder data

## 1.0.0-beta.9 — Apr 9, 2026
- **Exporter:** scan `_elementor_data` for image URLs and bundle them in the ZIP
- **Importer:** remap attachment IDs inside Elementor JSON (`"id":OLD` → `"id":NEW`)

## 1.0.0-beta.8 — Apr 9, 2026
- **Feature:** Post Type Mapping on import — override source post type (e.g., page → case_study)
- Mapping dropdown appears after ZIP upload, defaults to original type

## 1.0.0-beta.7 — Apr 9, 2026
- Added Help tab integration (user guide + FAQ in WP Help dropdown)
- Featured image fallback: use first content image when no featured image exists

## Earlier versions
- beta.1 through beta.6: initial beta releases, chunked export, select-all-pages, dark mode, PUC auto-updates via GitHub
