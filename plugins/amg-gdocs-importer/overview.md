---
title: Overview
parent: GDocs Importer
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG GDocs Importer pulls Google Docs directly into WordPress as draft posts, ready for the AMG Publisher pipeline. No more copy-pasting or third-party services.

## What it does

- Connects to a shared **Google Drive folder** via a service account
- **Search** for documents by title (no browsing giant folders)
- Imports Google Doc content as **Gutenberg-ready blocks** (headings, paragraphs, lists, images)
- Downloads and localizes Google Doc images into the WordPress media library
- Creates posts as the `wordable_import` post type (used by AMG Publisher)
- Detects already-imported docs to prevent duplicates

## When to use it

| Situation | Use GDocs Importer? |
|-----------|----------------------|
| Content team writes in Google Docs | Yes |
| Need to import a batch of blog posts | Yes |
| Need pixel-perfect formatting from Google Docs | No — formatting is converted to clean HTML blocks |
| Content is in Word files, not Google Docs | No — only Google Docs are supported |

## How it fits in the workflow

1. Writers create content in Google Docs (in the shared folder)
2. Designer searches for the doc in GDocs Importer → clicks Import
3. Doc becomes a `wordable_import` draft in WordPress
4. Designer opens it in **AMG Publisher** to build the final blog layout
5. Publisher creates the live post with featured image, template, and formatting
