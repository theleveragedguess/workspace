## 2024-10-27 - Icon-Only Button Accessibility
**Learning:** Found an icon-only `<Popover.Trigger>` in `CopyButton.tsx` that lacked an `aria-label`, making its function unclear to screen readers.
**Action:** Always ensure icon-only buttons (`<button>`, `<Popover.Trigger>`, etc.) have an `aria-label` attribute describing their action (e.g., `aria-label="Copy to clipboard"`).
