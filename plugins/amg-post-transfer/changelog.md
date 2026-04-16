---
title: Changelog
parent: Post Migration
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 1.0.0-beta.15 — Apr 14, 2026
- **Fix:** Windows-only bug where chunked exports produced ZIPs missing `manifest.json`. PHP's ZipArchive on Windows silently fails after many open/close cycles across separate PHP requests (the pattern chunked export uses). macOS libzip handles it fine; Windows does not.
- **Patch 1 (defensive):** Added return-value checks on `wp_json_encode()`, `addFromString()`, and `close()` — silent failures now return `WP_Error` instead of producing broken ZIPs. Defense-in-depth: verify `manifest.json` is actually present after close; write sidecar if missing.
- **Patch 2 (the real fix):** `finalize_job()` now does a **single-cycle rebuild** — opens the chunked ZIP read-only, extracts entries, creates a brand new ZIP at a temp path with media + manifest in one open/close cycle, then atomically swaps it into place. Windows-safe swap pattern avoids "pending-delete" state that blocks rename/copy.

## 1.0.0-beta.14 — Apr 14, 2026
- Switched to shared `AMG_Help_Tabs` class (provided by AMG Suite)
- Help docs now load from `AbstraktMG/amg-docs` with 24h cache, bundled help/ folder as fallback

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
