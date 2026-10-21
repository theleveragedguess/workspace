## 2024-05-18 - Missing ARIA Labels in Admin Tables
**Learning:** Found a recurring pattern in the admin marketplace section where icon-only action buttons within table rows (like "View App Details" and "Remove") were lacking `aria-label` attributes.
**Action:** Always ensure that any icon-only button, particularly in data grid or table action columns, explicitly provides an `aria-label` matching its intended function (e.g. `aria-label="Remove"`).
