## 2023-10-18 - Added ARIA labels to icon-only buttons
**Learning:** Found that there are numerous instances of `<button>` tags with only an `<Icon>` child and no `aria-label`. This makes these buttons completely inaccessible to screen readers, as they will just read out "button" without any context of what the button does. While tooltips provide context for visual users, screen readers need the `aria-label` directly on the button element.
**Action:** Always add `aria-label` to buttons that only contain an icon, even if they have a tooltip.
