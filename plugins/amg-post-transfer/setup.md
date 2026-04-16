---
title: Setup
parent: Post Migration
grand_parent: Plugins
nav_order: 2
---

# Setup

## Requirements

- WordPress 5.5+
- PHP 7.4+
- `AMG Suite` plugin active
- PHP `ZipArchive` extension (standard on most hosts)
- Write access to `/wp-content/uploads/`

## Installation

1. Download the latest `amg-post-transfer.zip` from your AMG distribution
2. WordPress Admin → Plugins → Add New → Upload Plugin
3. Activate
4. Verify it appears under **AMG → Post Migration**

## Auto-updates (optional)

If your site has `AMG_GITHUB_TOKEN` in `wp-config.php`, the plugin will auto-update when new versions are released to `AbstraktMG/amg-post-transfer`.

Add to `wp-config.php`:

```php
define('AMG_GITHUB_TOKEN', 'your_github_pat_here');
```

Without a token, the plugin still works — you just have to upload new ZIPs manually when they're released.
