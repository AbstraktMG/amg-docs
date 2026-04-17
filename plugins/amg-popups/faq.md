---
title: FAQ
parent: Popups & Sticky Bars
grand_parent: Plugins
nav_order: 4
---

# FAQ

### How do I test a popup without cookies blocking it?
Set the Cookie Duration to **Test Mode (0 days)** in the Targeting tab. The popup will show every time you reload the page.

### Can I use shortcodes in popup content?
Yes. The content editor supports shortcodes, HTML, and media.

### Why isn't my popup showing?
Check:
1. Is the status set to **Active**?
2. Does the targeting match the page you're viewing? (site-wide, post type, or specific page)
3. Is there a cookie blocking it? Clear cookies or use Test Mode.
4. For button-click triggers: does the HTML element ID match?

### Can I have multiple popups on one page?
Yes. Each popup fires independently based on its trigger.

### What's the difference between exit intent and inactivity?
**Exit intent** fires when the mouse physically leaves the top of the browser window (desktop only — doesn't work on mobile). **Inactivity** fires when the user stops interacting (no mouse, keyboard, scroll, or touch) for the configured seconds.

### Does exit intent work on mobile?
No. Exit intent relies on mouse tracking, which isn't available on touch devices. Use timed delay or scroll depth for mobile-friendly triggers.

### Can I add a logo to a popup?
Logos are only available for sticky bars (top/bottom bars). Use the Logo URL and Logo Position fields in the Style tab.

### How do I trigger a popup from a button?
1. Set the trigger to **Button Click**
2. Enter an element ID (e.g., `my-popup-trigger`)
3. Add `id="my-popup-trigger"` to any HTML element on the page (button, link, div)
