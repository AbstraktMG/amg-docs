---
title: Setup
parent: Media Cleaner
grand_parent: Plugins
nav_order: 2
---

# Setup

## Requirements

- WordPress 5.0+
- PHP 7.4+
- **AMG Suite** plugin active

## Installation

1. Download `amg-media-cleaner.zip`
2. WordPress Admin → Plugins → Add New → Upload Plugin
3. Activate
4. Find it under **AMG → Media Cleaner**

## First scan

No configuration needed. Go to **AMG → Media Cleaner** and click **Scan Now**. The first scan takes longer (it builds a full reference index of your site), subsequent scans are faster.

## Database tables

The plugin creates two custom tables on activation:
- `{prefix}_amc_references` — index of all found media references
- `{prefix}_amc_scan_results` — scan findings

These are cleaned up on uninstall.
