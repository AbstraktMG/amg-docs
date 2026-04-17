---
title: Usage
parent: Excerpts
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

**AMG → Excerpts**

The plugin has two tabs: **Excerpts** (main workspace) and **Settings**.

---

## Excerpts tab

### Summary cards

At the top you'll see three numbers:

- **Total Posts** — all posts in your selected post types
- **With Excerpts** — posts that already have an excerpt
- **Missing Excerpts** — posts without an excerpt (this is what you're here to fix)

### Preview table

Below the summary is a table showing every post with:

- Post title (links to the editor)
- Post type
- Current excerpt (if any)
- SEO meta description (from Yoast/AIOSEO)
- Status badge
- **Sync** button — click to sync that individual post (overwrites existing excerpt)

Use the search box and status filter to find specific posts.

### Bulk processing

Two buttons at the top:

**Run Excerpt Creator** (safe mode)
- Only fills posts that have **no excerpt**
- Skips posts with existing excerpts — won't overwrite your manual work
- Use this first

**Force Sync All**
- Overwrites **every** excerpt with the current SEO meta description
- Shows a confirmation dialog before running
- Use this when you've updated SEO descriptions and want to push changes to excerpts

Both modes show a progress bar and a live results log. Each post shows its status:

| Status | Meaning |
|--------|---------|
| Updated | Excerpt was filled from SEO meta |
| Skipped | Post already has an excerpt (safe mode only) |
| No meta | No SEO description found for this post |
| Error | Something went wrong |

You can click **Cancel** at any time to stop the bulk run.

### Auto-sync on publish

When you publish or schedule a post, the plugin automatically fills the excerpt from the SEO description — but only if the excerpt field is empty. It never overwrites a manual excerpt on publish.

---

## Settings tab

### Post types

Check which post types to include. Only checked types appear in the summary, preview table, and bulk processing.

### SEO source

- **Auto-detect** (recommended) — tries Yoast first, then AIOSEO
- **Yoast only** — only reads from Yoast SEO
- **AIOSEO only** — only reads from All in One SEO

Click **Save Settings** after making changes.
