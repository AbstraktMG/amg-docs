---
title: Overview
parent: Excerpts
grand_parent: Plugins
nav_order: 1
---

# Overview

AMG Excerpts syncs SEO meta descriptions (from Yoast SEO or All in One SEO) to WordPress excerpts across your site. It fills the excerpt field automatically so you don't have to copy-paste from your SEO plugin.

## What it does

- Reads SEO meta descriptions from **Yoast SEO** or **AIOSEO**
- Copies them into the WordPress excerpt field
- Supports **bulk processing** — fill hundreds of excerpts in one click
- **Auto-syncs on publish** — new posts get their excerpt filled automatically
- Respects manual excerpts — won't overwrite unless you tell it to

## When to use it

| Situation | Use Excerpts? |
|-----------|---------------|
| You have SEO meta descriptions but empty excerpts | Yes — bulk fill them |
| Theme or plugin needs excerpts for archive pages | Yes |
| You wrote custom excerpts and want to keep them | Yes — safe mode skips existing |
| You want to overwrite all excerpts with fresh SEO data | Yes — use Force Sync |
| You don't use Yoast or AIOSEO | No — the plugin needs one of these as a source |

## Supported SEO plugins

- **Yoast SEO** (reads `_yoast_wpseo_metadesc`)
- **All in One SEO** (both v4+ API and legacy `_aioseop_description`)
- Auto-detect mode tries Yoast first, falls back to AIOSEO
