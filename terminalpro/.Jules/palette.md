## 2024-05-18 - Missing ARIA labels on icon-only buttons
**Learning:** Found a systemic accessibility issue across the terminalpro application where icon-only buttons (like `CopyButton` and info icons in `Settings`) lack `aria-label` attributes, making them inaccessible to screen readers.
**Action:** Always ensure that buttons whose content is purely visual (icons, SVGs) include an explicit, descriptive `aria-label` attribute.
