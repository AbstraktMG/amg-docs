---
title: FAQ
parent: AMG Suite
grand_parent: Plugins
nav_order: 4
---

# FAQ

### Do I need AMG Suite to use the child plugins?
Yes. All AMG child plugins check for `AMG_SUITE_ACTIVE` and register their menu under the AMG parent. Without Suite, they show an admin notice but don't crash.

### What happens if I deactivate AMG Suite?
Child plugin menus disappear from the sidebar, but the plugins themselves keep working. They'll show admin notices asking you to reactivate Suite.

### What does the Remote Config do?
It fetches shared API credentials and version targets from a central GitHub repo. This lets you update keys (like the Google service account) once and have all 200+ sites pick it up automatically, instead of configuring each site individually.

### What if AMG_GITHUB_TOKEN isn't set?
Everything still works — child plugins fall back to their local settings (database or manual configuration). You just don't get remote config sync or auto-update notifications.

### How often does the config refresh?
Daily via WordPress cron. You can also click **Refresh Now** on the dashboard for an immediate fetch.

### What do the version badge colors mean?
- **Green** — installed version matches or exceeds the target in remote config
- **Amber** — installed version is older than the target (update available)
- **No badge** — plugin not installed or version can't be determined

### Is the remote config encrypted?
Yes. API credentials are encrypted with AES-256-CBC using your site's `wp_salt('auth')` before storage in `wp_options`. They're never exposed in the admin UI.
