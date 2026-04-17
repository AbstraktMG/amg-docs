---
title: Troubleshooting
parent: AMG Suite
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| "AMG_GITHUB_TOKEN not set" warning | Token not in wp-config.php | Add `define('AMG_GITHUB_TOKEN', '...');` to wp-config.php |
| Config status shows "stale" | Cron hasn't run or token is invalid | Click Refresh Now; verify token has read access to AbstraktMG repos |
| Config refresh fails | Token expired or revoked | Generate a new GitHub PAT and update wp-config.php |
| Child plugin not showing in AMG menu | AMG Suite not active, or plugin has a fatal error | Check that Suite is active; check the plugin's error log |
| All version badges are green even though versions differ | No remote config (token not set) | Without remote config, badges default to green (no comparison data) |
| Dashboard crashes on load | `class-remote-config.php` missing from `includes/` | Re-upload the full amg-suite.zip (ensure includes/ folder is present) |

## Remote Config debugging

If config isn't fetching:
1. Verify `AMG_GITHUB_TOKEN` is defined in wp-config.php
2. Test the token: `curl -H "Authorization: token YOUR_TOKEN" https://api.github.com/user`
3. Verify repo access: `curl -H "Authorization: token YOUR_TOKEN" https://api.github.com/repos/AbstraktMG/amg-config`
4. Check `wp_options` for `amg_suite_config_updated` — should show a recent timestamp
5. Check `wp-content/debug.log` for `[AMG Config]` entries (if WP_DEBUG is enabled)
