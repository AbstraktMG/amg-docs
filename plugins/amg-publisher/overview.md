---
title: Overview
parent: Post Publisher
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG Publisher builds polished blog posts from imported content. It takes raw imported documents (from GDocs Importer or other sources) and converts them into fully structured WordPress posts with page builder layouts, featured images, and SEO metadata.

## What it does

- Converts `wordable_import` draft posts into published blog posts
- Builds layouts for **Enfold** (shortcodes) or **Elementor** (containers + widgets)
- Applies one of **3 content templates** (A, B, C) with headers, columns, and styling
- Sets **featured images**, **categories**, and **Yoast SEO metadata**
- Supports full-width headers with image, video, or solid color backgrounds
- **Drag-and-drop** content assembly in the builder page

## How it fits in the workflow

1. Content is imported via **GDocs Importer** → creates a `wordable_import` draft
2. Designer opens the import in **AMG Publisher** → clicks "Build Layout"
3. Selects template, featured image, categories, and SEO data
4. Publisher converts the raw content into a structured page builder layout
5. Saves as a new published (or draft) `post` and trashes the original import

## Supported builders

The plugin auto-detects the active theme:
- **Enfold theme** → builds Enfold/Avia shortcodes
- **Other themes** → builds Elementor containers and widgets
