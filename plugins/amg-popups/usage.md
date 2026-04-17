---
title: Usage
parent: Popups & Sticky Bars
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

**AMG → Popups**

---

## Creating a popup or sticky bar

1. Click **Add New**
2. Choose **Popup** or **Sticky Bar** from the Type dropdown
3. Fill in the 4 tabs:

### Content tab
- **Title** — internal name (not shown to visitors)
- **Content** — WYSIWYG editor with full WordPress formatting, media, and shortcode support

### Trigger tab
- **Trigger type** — choose when the popup appears:
  - **Button Click** — enter the HTML element ID (e.g., `open-popup`)
  - **Exit Intent** — fires when mouse leaves the viewport top
  - **Timed Delay** — fires after X milliseconds (default: 5000 = 5 seconds)
  - **Scroll Depth** — fires when scrolled past X% (default: 50%)
  - **Inactivity** — fires after X seconds of no activity (default: 30 seconds)

### Style tab
- **Width** — popup width in pixels (default: 600px)
- **Background color** — popup/bar background
- **Padding** — inner spacing
- **Shadow** — color and size
- **Overlay** — backdrop color and opacity (popups only)
- **Position** — center, top-left, top-right, bottom-left, bottom-right (popups) or top/bottom (sticky bars)
- **Animation** — fade, slide from any direction (popups) or fade, slide, spread (sticky bars)
- **Sticky bar extras** — text alignment, logo URL, logo position

### Targeting tab
- **Site-wide** — show on every page (overrides other rules)
- **Post Types** — show on all posts of selected types
- **Specific Pages** — search and select individual pages/posts by title
- **Cookie Duration** — how long to suppress after dismissal:
  - Test Mode (always show)
  - 1 Day, 1 Week, 2 Weeks, 1 Month, 3 Months, 1 Year

4. Click **Save**

---

## Managing popups

The list view shows all popups with:
- Title, type, trigger, targeted pages, status
- **Edit** — open the editor
- **Duplicate** — copy all settings (creates as inactive)
- **Delete** — remove with confirmation
- **Status toggle** — activate/deactivate without editing

---

## How visitors interact

**Popups:**
- Appear based on the trigger condition
- Dark overlay behind the popup
- Close via: X button, clicking overlay, pressing Escape
- Page scroll is locked while popup is open
- Cookie set on close — won't show again within the configured duration

**Sticky Bars:**
- Appear fixed to the top or bottom of the viewport
- Close via X button
- Page remains scrollable
- Cookie set on close
