---
title: Usage
parent: AMG Suite
grand_parent: Plugins
nav_order: 3
---

# Usage

## Dashboard

**AMG → Dashboard**

### Remote Config status

At the top, a status bar shows:
- **Config version** and last update time
- **Stale warning** if config hasn't refreshed in 48+ hours
- **Refresh Now** button for immediate update
- **"AMG_GITHUB_TOKEN not set"** if no token is configured

### Plugin cards

Each installed AMG plugin shows a card with:
- **Plugin name** and description
- **Active / Inactive** badge
- **Version badge** — green if current, amber if outdated (compared to remote config targets). Hover amber badges to see the latest version.
- **Open** button (if active) or **Activate** link (if inactive)

### Dark mode

Click the ☀/☽ toggle in the top-right corner. Persists across sessions via localStorage.

---

## Installing child plugins

1. Download the child plugin ZIP
2. Upload via Plugins → Add New → Upload Plugin
3. Activate
4. It appears automatically under the AMG menu

No registration or configuration needed — child plugins detect AMG Suite automatically.

---

## Updating plugin versions

When you ship a new version of any AMG plugin:

1. Bump the `Version:` header in the plugin's main PHP file
2. Push to the plugin's GitHub repo
3. Update `plugin_versions` in `AbstraktMG/amg-config/config.json` with the new version number
4. Commit and push config.json

All sites will show the amber "outdated" badge within 24 hours (or on manual Refresh).
