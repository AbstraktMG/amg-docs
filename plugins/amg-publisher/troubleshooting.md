---
title: Troubleshooting
parent: Post Publisher
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| "Build Layout" link missing | Post is not a `wordable_import` type | Only imports show the build action |
| Builder page says "not allowed" | Menu registration issue with `show_in_menu` | Update to latest version (fixed in v2.0.3+) |
| Enfold shortcodes showing as raw text | Enfold theme not active | Activate Enfold, or switch to Elementor mode |
| Featured image not setting | Attachment ID missing or invalid | Select a new image from the media library in the builder |
| SEO metadata not saving | Yoast SEO not installed | Install and activate Yoast SEO |
| Layout looks wrong after publishing | Template doesn't match content structure | Try a different template (A, B, or C) |
| Images missing in published post | Image references from import are broken | Use AMG Post Transfer to re-import with media, or fix manually |

## Template tips

- **Template A** works best for standard blog posts with a single content flow
- **Template B** is good for posts that need a sidebar with related content
- **Template C** works for longer posts with visual variety (alternating column layouts)
