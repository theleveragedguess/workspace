## 2024-10-26 - Add ARIA Labels to AdminMarketplace Icon-Only Buttons
**Learning:** Found several icon-only buttons in AdminMarketplace (`AppsTab.tsx` and `WhitelistTab.tsx`) missing `aria-label` attributes, which impairs screen reader accessibility for administrative tasks.
**Action:** Always ensure `aria-label` is included for buttons containing only icons to provide semantic context for assistive technologies.
