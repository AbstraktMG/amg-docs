---
title: Troubleshooting
parent: Popups & Sticky Bars
grand_parent: Plugins
nav_order: 5
---

# Troubleshooting

## Common issues

| Problem | Likely cause | Fix |
|---------|-------------|-----|
| Popup not showing | Inactive status or cookie blocking | Check status is Active; clear cookies or set Test Mode |
| Popup shows on wrong pages | Targeting misconfigured | Check site-wide toggle, post type selections, and page slugs |
| Button click trigger not working | Element ID mismatch | Verify the ID in the trigger matches the ID on the HTML element exactly (case-sensitive) |
| Exit intent not firing | Using mobile device | Exit intent only works on desktop (mouse-based). Use timed delay for mobile. |
| Popup appears behind other content | Z-index conflict with theme | Contact developer — the popup uses a high z-index but some themes override |
| Sticky bar overlaps site header | Bar set to top position | Adjust the site's header CSS or switch bar to bottom position |
| Content not saving | TinyMCE editor issue | Switch to Text mode, paste content, switch back to Visual, then save |
| Duplicate popup showing old content | Browser cache | Hard refresh (Ctrl+Shift+R) or clear cache |

## Cookie behavior

- Cookies are named `apc-popup-{id}` where `{id}` is the popup database ID
- Set when the popup is closed (X button, overlay click, or Escape key)
- Duration follows the Cookie Duration setting in the Targeting tab
- To force-clear: open browser DevTools → Application → Cookies → delete `apc-popup-*` entries
