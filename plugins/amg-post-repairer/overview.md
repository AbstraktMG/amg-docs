---
title: Overview
parent: Post Repairer
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG Post Repairer scans, converts, and repairs post content across page builders. When migrating sites between themes or builders, content often breaks — shortcodes don't render, images lose their references, and layouts fall apart. This plugin fixes that.

## What it does

- **Scans** posts to detect which page builder created them (Enfold, Elementor, Divi, WPBakery, Oxygen, Gutenberg)
- **Converts** content between builders (e.g., Enfold → Gutenberg, Elementor → Enfold)
- **Repairs images** — fixes broken attachment IDs, downloads missing images from the source site
- **Repairs styling** — restores heading/body colors and sidebar layouts for Enfold posts
- **Backs up** original content before converting — restore anytime

## Supported builders

| Builder | Detect | Convert From | Convert To |
|---------|--------|-------------|------------|
| Enfold | Yes | Yes | Yes |
| Elementor | Yes | Yes | Yes |
| Divi | Yes | Yes | No |
| WPBakery | Yes | Yes | No |
| Oxygen | Yes | No | No |
| Gutenberg | Yes | Yes | Yes |
| Raw HTML | Yes | Yes | Yes |

## When to use it

| Situation | Use Post Repairer? |
|-----------|---------------------|
| Migrated from Enfold to a Gutenberg theme | Yes — convert Enfold shortcodes to blocks |
| Imported posts with broken images | Yes — repair image references |
| Content shows raw shortcodes like `[av_section]` | Yes — convert to the active builder |
| Need to bulk-fix styling after a theme change | Yes — repair colors and sidebar settings |
| Building a new site from scratch | No — nothing to repair |
