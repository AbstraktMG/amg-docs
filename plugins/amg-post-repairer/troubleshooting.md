---
title: Troubleshooting
parent: Post Repairer
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| Conversion produces empty content | Source had only builder-specific elements with no text content | Check original post; restore from backup if needed |
| Empty `av_one_full` sections in Enfold | Source blocks had no heading, paragraph, image, or CTA content | Known issue — converter skips empty blocks |
| Images show in frontend but not in Enfold ALB | Shortcode tree doesn't fully match the content | Known limitation — images may need manual placement in ALB |
| `av_image` shows broken image | Attachment ID points to a deleted/missing file | Run Repair Images with a source URL configured |
| "Error" status after conversion | Conversion produced empty output from non-empty input | Check the source content format; try a different target builder |
| Scan shows "Unknown" builder | Content doesn't match any known builder pattern | Content may be raw HTML — convert from Raw HTML |
| Colors not applying | Heading/body color fields empty in settings | Set hex values in the settings panel before running color repair |

## Known limitations

1. **Enfold ALB image display** — images may show on the frontend but not render in the Enfold Advanced Layout Builder editor. This is an ongoing issue with how the shortcode tree is built.
2. **Complex nested layouts** — deeply nested columns and grids from Elementor/Divi may simplify during conversion. Manual adjustment may be needed.
3. **Oxygen builder** — detection only, no converter. Content is extracted as raw HTML.
4. **Custom CSS/styling** — builder-specific custom CSS is not carried over during conversion.

## Image repair strategy

The image fixer works in order:
1. **Local lookup** — search WordPress media library by filename
2. **Remote download** — if Source Site URL is set, try downloading from the original location
3. **Placeholder** — if configured, use the placeholder image
4. **Give up** — increment the missing count, leave the reference broken

Configure both Source Site URL and Placeholder Image in settings for best results.
