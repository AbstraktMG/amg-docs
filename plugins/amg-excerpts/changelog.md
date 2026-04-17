---
title: Changelog
parent: Excerpts
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 1.0.0-beta.7
- GitHub token support for private repo auto-updates (PUC)

## 1.0.0-beta.6
- Fix: row Sync button now correctly force-overwrites (was skipping posts with existing excerpts)

## 1.0.0-beta.5
- Feature: "Force Sync All" button with overwrite confirmation dialog
- Added `get_all_post_ids()` for fetching all posts regardless of excerpt status

## 1.0.0-beta.4
- Fix: guard excerpt generator against overwriting existing excerpts (safe-by-default)
- Added `$force` parameter to `generate_excerpt()`

## 1.0.0-beta.3
- Segmented pill dark mode toggle (☀/☽)
- FOUC prevention via inline preload script
- Changed toggle from `<button>` to `<div>` to avoid WP admin button styling

## 1.0.0-beta.1
- Initial beta release
- Bulk excerpt sync from Yoast/AIOSEO
- Auto-sync on publish
- Preview table with search and filtering
- Dark mode support
