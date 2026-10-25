## 2024-05-15 - Widespread Missing ARIA Labels on Icon-only Buttons
**Learning:** Found a recurring pattern where actionable icon-only buttons (like Trash/Delete and Info icons) across multiple settings and admin tabs were missing `aria-label`s. This makes them functionally invisible to screen readers, violating a11y standards for an enterprise tool.
**Action:** Always ensure that `<button>` wrappers around `<Icon />` components include an explicit, descriptive `aria-label` attribute (e.g., "Remove parameter" instead of just having a trash icon).
