---
title: Troubleshooting
parent: Excerpts
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| All posts show "No meta" | SEO plugin not active or no descriptions filled | Check that Yoast or AIOSEO is active and posts have meta descriptions |
| Summary shows 0 total posts | Wrong post types selected | Go to Settings and check the correct post types |
| Bulk run skips everything | Posts already have excerpts | Use "Force Sync All" if you want to overwrite |
| Individual Sync button not working | JavaScript error | Check browser console; try clearing cache |
| Plugin not visible in AMG menu | AMG Suite not active | Activate AMG Suite first |
| Auto-sync not working on publish | Post type not checked in settings | Add the post type in Settings |

## Force Sync safety

Before using "Force Sync All" on a large site:

1. Take a database backup
2. Test on a few posts first using the individual Sync button
3. Verify the SEO descriptions are what you want as excerpts
4. Then run the full sync
