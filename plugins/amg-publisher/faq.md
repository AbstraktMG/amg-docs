---
title: FAQ
parent: Post Publisher
grand_parent: Plugins
nav_order: 4
---

# FAQ

### Where do the imports come from?
The `wordable_import` posts are created by **AMG GDocs Importer** (or any process that creates posts of that type). The Publisher then converts them into published blog posts.

### How does it know to use Enfold vs Elementor?
It checks if the Enfold theme is active. If yes, it builds Enfold shortcodes. Otherwise, it builds Elementor containers and widgets.

### Can I edit the post after publishing?
Yes. The published post is a standard WordPress post — edit it normally in Gutenberg, Enfold ALB, or Elementor.

### What if I don't like the result?
The original import is in the trash — restore it and try a different template.

### Does it set a featured image automatically?
It uses the featured image from the import metadata. You can also select a different image in the builder.

### Can I change the template after publishing?
Not through the Publisher. You'd need to edit the post directly in the page builder, or restore the import and re-build with a different template.

### Does it work with themes other than Enfold?
Yes — it falls back to Elementor for non-Enfold themes. Elementor must be installed.

### What's a `wordable_import`?
A custom post type used as a staging area for imported content. It holds the raw content until you build it into a published post.
