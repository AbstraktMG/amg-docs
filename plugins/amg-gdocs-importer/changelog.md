---
title: Changelog
parent: GDocs Importer
grand_parent: Plugins
nav_order: 6
---

# Changelog

## 1.0.0-beta.7 — Apr 14, 2026
- Auth now checks AMG Suite Remote Config as a credential source (priority: wp-config constant → remote config → DB setting)

## 1.0.0-beta.6
- Dark mode: segmented pill toggle, FOUC prevention
- UI polish

## 1.0.0-beta.2
- Build script (`build.sh`) strips 640 unused Google services from vendor (226MB → 2.3MB ZIP)
- `.gitignore` added for vendor/ and build/

## 1.0.0-beta.1
- Search-first UI (no longer lists entire folder)
- Optimized import-check from N queries to single SQL
- Batch import with progress bar

## Earlier versions
- Alpha releases with folder browsing UI (replaced by search-first approach)
