---
title: Setup
parent: Post Repairer
grand_parent: Plugins
nav_order: 2
---

# Setup

## Requirements

- WordPress 5.0+
- **AMG Suite** plugin active
- The **target page builder** should be installed (e.g., if converting to Enfold, Enfold theme should be active)

## Installation

1. Download `amg-post-repairer.zip`
2. WordPress Admin → Plugins → Add New → Upload Plugin
3. Activate
4. Find it under **AMG → Post Repairer**

## Configuration

Before running repairs, configure the settings panel (click to expand):

1. **Target Builder** — which builder to convert to (Enfold, Elementor, or Gutenberg)
2. **Post Types** — which post types to include (default: Posts and Pages)
3. **Heading Color** — optional hex color to apply to headings during conversion
4. **Body Text Color** — optional hex color for paragraph text
5. **Sidebar Layout** — None, Right, or Left sidebar for Enfold conversions
6. **Placeholder Image** — fallback image for broken/missing images that can't be found or downloaded
7. **Source Site URL** — original domain to attempt downloading missing images from (e.g., `https://oldsite.com`)
