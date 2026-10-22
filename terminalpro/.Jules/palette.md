## 2025-05-18 - Missing ARIA Labels on Table Action Buttons
**Learning:** Icon-only action buttons within table rows (like those in AdminMarketplace) frequently lack `aria-label`s, making them invisible or unclear to screen reader users. This happens because tooltips are used for visual context, but developers sometimes forget to add screen reader context directly on the interactive button element.
**Action:** Audit icon-only buttons across the app, especially in data tables or repetitive lists. Ensure that every `<button>` wrapping an `<Icon>` includes a descriptive `aria-label`.
