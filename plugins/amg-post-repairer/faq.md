---
title: FAQ
parent: Post Repairer
grand_parent: Plugins
nav_order: 4
---

# FAQ

### Will this overwrite my content?
Yes — conversion replaces post content with the converted version. But a backup is always created first, and you can restore anytime.

### What happens to unsupported shortcodes?
Shortcodes the converter doesn't recognize are stripped. The raw content inside them is preserved as paragraphs where possible.

### Can I convert from Enfold to Elementor?
Yes. The plugin supports converting from any detected builder to Enfold, Elementor, or Gutenberg.

### What if images are missing after conversion?
Run **Repair Images**. It tries three approaches:
1. Find the image by filename in the local media library
2. Download from the source site URL (if configured)
3. Use the placeholder image (if configured)

### Does it handle Enfold's Advanced Layout Editor (ALB)?
Partially. The converter builds Enfold shortcodes and the shortcode tree, but some complex layouts (nested columns, custom styling) may need manual adjustment in the ALB editor.

### Can I run it on custom post types?
Yes. Check the post types you want in the Settings panel.

### How long does conversion take?
Each post is processed individually via AJAX. A batch of 100 posts takes a few minutes. Complex posts with many images take longer.

### Is there an undo?
Yes — every conversion creates a backup. Use **Restore from backup** to revert.

### What if the same builder is source and target?
The plugin runs repairs instead of a full conversion — fixing images, colors, and sidebar without re-converting the content structure.
