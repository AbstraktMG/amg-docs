---
title: Setup
parent: AMG Suite
grand_parent: Plugins
nav_order: 2
---

# Setup

## Requirements

- WordPress 5.0+
- PHP 7.4+

## Installation

1. Download `amg-suite.zip`
2. WordPress Admin → Plugins → Add New → Upload Plugin
3. Activate
4. The "AMG" menu appears in the sidebar

## Auto-updates (optional)

To enable auto-updates from private GitHub repos:

Add to `wp-config.php`:
```php
define('AMG_GITHUB_TOKEN', 'your_github_pat_here');
```

Create a fine-grained GitHub Personal Access Token at [github.com/settings/tokens](https://github.com/settings/tokens) with:
- **Resource owner:** AbstraktMG
- **Repositories:** All AMG repos (or selected)
- **Permissions:** Contents (read-only), Metadata (read-only)

Without a token: plugins still work, just no auto-update notifications for private repos.

## Remote Config

If `AMG_GITHUB_TOKEN` is set, AMG Suite automatically fetches shared API credentials from `AbstraktMG/amg-config`:
- Google service account (for GDocs Importer)
- SEMrush, GTmetrix, Teams webhook keys (for future plugins)
- Plugin version targets (for dashboard version badges)

Config is fetched on activation and refreshed daily via cron. Click **Refresh Now** on the dashboard for immediate updates.
