---
title: Changelog
parent: Post Repairer
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 1.0.0-beta.8
- GitHub token support for private repo auto-updates

## 1.0.0-beta.7
- Empty block guard: skip blocks with no content (heading, paragraph, image, or CTA)
- Removed spacer spam between blocks
- Image attachment ID resolution: extracts `wp-image-{id}` from CSS class, `resolve_attachment_id()` fallback via `attachment_url_to_postid()`
- Shortcode tree build for Enfold ALB via `ShortcodeHelper::build_shortcode_tree()`
- Still unresolved: images show on frontend but not in Enfold ALB editor

## 1.0.0-beta.6
- Dark mode toggle (segmented pill ☀/☽)
- FOUC prevention

## Earlier versions
- beta.1 through beta.5: Core scanning, conversion (Enfold/Elementor/Gutenberg), image repair, color repair, backup/restore, bulk AJAX processing
