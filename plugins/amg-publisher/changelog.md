---
title: Changelog
parent: Post Publisher
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 2.0.5
- GitHub token support for private repo auto-updates

## 2.0.4
- Bug fixes and stability improvements

## 2.0.3
- Fix: builder page "not allowed" error — `show_in_menu => false` was hiding the CPT menu and breaking the submenu parent. Fixed with `null` parent + `admin.php?page=` URL.
- DOMDocument warnings on HTML5 tags suppressed with `@$doc->loadHTML()`

## 2.0.0
- Elementor container support (migrated from legacy sections to modern containers)
- Template builders: `build_template_a/b/c()` for Elementor
- Widget helpers: `e_heading()`, `e_text()`, `e_image()`, `e_button()`, `e_divider()`

## Earlier versions
- 1.x: Enfold-only builder, drag-drop content assembly, Yoast integration, category mapping
