---
title: Changelog
parent: AMG Suite
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 1.0.8 — Apr 14, 2026
- Shared Help Tabs class (`AMG_Help_Tabs`) — child plugins register for contextual docs in WP Help dropdown
- Help content loaded from `AbstraktMG/amg-docs` with 24h cache, bundled help/ folder as fallback
- Markdown-to-HTML converter with headings, tables, lists, links, blockquotes

## 1.0.7 — Apr 14, 2026
- **Feature:** Plugin version badges on dashboard cards
- Green badge if installed version matches remote config target, amber if outdated
- Hover amber badges to see the latest version number
- `plugin_versions` map added to remote config

## 1.0.6 — Apr 13, 2026
- **Feature:** Remote Config system (`AMG_Remote_Config`)
- Fetches `config.json` from `AbstraktMG/amg-config` via GitHub API
- Encrypted cache in `wp_options` (AES-256-CBC)
- Daily cron refresh + manual "Refresh Now" button
- Dashboard status indicator (version, last updated, stale warning)
- GDocs Importer updated to check remote config for Google credentials

## 1.0.5
- GitHub token support for Plugin Update Checker (private repo auto-updates)

## 1.0.4
- Dark mode: segmented pill toggle (☀/☽), FOUC prevention via inline preload script

## 1.0.3
- Plugin Update Checker v5.6 (clean install, replacing corrupted earlier version)

## 1.0.2
- Initial release with modern dashboard and plugin card list
