---
title: FAQ
parent: Excerpts
grand_parent: Plugins
nav_order: 4
---

# FAQ

### Will this overwrite my manually written excerpts?
Not by default. The "Run Excerpt Creator" button only fills **empty** excerpts. Use "Force Sync All" only when you intentionally want to overwrite everything.

### What if I don't have Yoast or AIOSEO?
The plugin won't find any SEO descriptions to sync. You'll see "No meta" status for every post. Install one of the supported SEO plugins first.

### Does it work with RankMath?
Not currently. Only Yoast SEO and All in One SEO are supported.

### Can I use it with custom post types?
Yes. Go to Settings → check the custom post types you want to include.

### What happens when I publish a new post?
The plugin automatically fills the excerpt from the SEO description — but only if the excerpt field is empty. It won't touch it if you already wrote one.

### Can I undo a bulk sync?
No. There's no built-in undo. If you accidentally overwrote excerpts with "Force Sync All," you'd need to restore from a backup.

### Why does a post show "No meta"?
That post doesn't have an SEO meta description set in Yoast or AIOSEO. Fill in the SEO description first, then sync.

### Does the Sync button in the preview table overwrite?
Yes. The individual Sync button always overwrites the existing excerpt, regardless of safe/force mode. Use it when you want to update a specific post.

### How many posts can it handle?
It processes one post per AJAX call, so it works on any size site. A bulk run of 500 posts takes about a minute.
