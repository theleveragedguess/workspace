## 2024-10-25 - React useMemo Optimization
**Learning:** Combining expensive mapping/filtering operations (e.g. deduplicating servers) and cheap operations (e.g. string matching) in a single `useMemo` that depends on frequently changing variables (like search query keystrokes) causes major performance bottlenecks.
**Action:** Always split `useMemo` blocks so that expensive operations only depend on rarely changing variables, while the cheap filtering logic operates on the pre-computed results using the frequently changing variables.
