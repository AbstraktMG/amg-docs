---
title: Overview
parent: AMG Suite
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG Suite is the master plugin for the Abstrakt Marketing Group WordPress tool suite. It provides a unified admin menu, a central dashboard, remote configuration management, and shared services for all AMG child plugins.

## What it does

- **Single admin menu** — all AMG plugins appear under one "AMG" menu item
- **Dashboard** — shows all plugins at a glance with status badges and version indicators
- **Remote Config** — fetches shared API credentials (Google, SEMrush, GTmetrix) from a central GitHub repo, encrypted and cached locally
- **Version badges** — green when current, amber when outdated, compared against the central config
- **Shared Help Tabs** — provides contextual documentation inside each plugin's admin page
- **Dark mode** — toggle between light and dark themes

## Plugin ecosystem

| Plugin | What it does |
|--------|--------------|
| GDocs Importer | Pull Google Docs into WordPress |
| Post Publisher | Build blog layouts from imported content |
| Excerpts | Sync SEO descriptions to excerpts |
| Post Repairer | Fix content across page builders |
| Media Cleaner | Find and remove unused media |
| Post Migration | Export/import posts between sites |
| Popups & Sticky Bars | Create targeted popups and bars |

Each plugin registers itself as a submenu under AMG Suite. If Suite isn't active, child plugins show an admin notice prompting installation.
