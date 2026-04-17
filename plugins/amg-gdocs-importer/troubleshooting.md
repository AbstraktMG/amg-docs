---
title: Troubleshooting
parent: GDocs Importer
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| "Connection test failed" | Bad credentials or folder not shared | Re-paste JSON, verify folder sharing, check APIs are enabled |
| "No service account configured" | No credentials in any of the 3 sources | Add via Remote Config, Settings UI, or wp-config.php |
| Search returns no results | Folder ID wrong, or docs are in subfolders | Verify folder ID; search checks the root folder |
| Import hangs on large docs | Timeout on image downloads | Check server timeout settings; try smaller docs first |
| Images missing in imported post | Image download blocked by SSRF protection | Only HTTPS images from Google domains are allowed |
| "Request failed" on new install | Service account not configured or vendor files missing | Re-upload plugin ZIP; check Settings for credentials |
| Plugin is 200MB+ | All Google API services included | Use the `build.sh` script to strip unused services (reduces to ~5MB) |

## SSRF protection

The plugin only downloads images from Google's domains (`*.googleusercontent.com`, `*.google.com`) over HTTPS. External images embedded in Google Docs are skipped for security.

## Build script for size reduction

The plugin's vendor directory includes all 640 Google API services. Only Drive and Docs are needed. Run the build script to strip the rest:

```bash
cd amg-gdocs-importer
./build.sh
# Output: build/amg-gdocs-importer.zip (~5MB instead of 200MB+)
```
