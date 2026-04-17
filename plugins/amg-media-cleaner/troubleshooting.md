---
title: Troubleshooting
parent: Media Cleaner
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| Scan finds 0 results | Site has no unused media, or scan didn't complete | Check that the scan finished all phases |
| Scan stalls at a phase | Server timeout during large batch | Click "Resume Scan" to continue from where it stopped |
| False positives (flagged media is actually used) | Media referenced in hardcoded template or CSS | Check the file before deleting; use trash first |
| "Permission denied" on delete | Server file permissions | Check that WordPress has write access to the uploads folder |
| Broken attachments showing up | Files deleted outside WordPress (FTP, host cleanup) | These are safe to delete — they're just orphaned DB records |
| Images from CDN/offload plugin flagged | WP Offload Media or WP Stateless in use | The scanner detects these and skips them — update to latest version if still happening |

## Before a large cleanup

1. **Back up your database and uploads folder**
2. Run the scan and **export CSV** first
3. Trash items instead of permanently deleting
4. Test the site thoroughly
5. Then permanently delete from the Trash tab
