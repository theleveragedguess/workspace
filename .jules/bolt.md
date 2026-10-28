## 2024-10-28 - Avoid List Lookups in Loops
**Learning:** Using `in` or `not in` on a list inside a loop leads to O(n^2) complexity, which can be a severe bottleneck for large inputs such as bulk dashboard/chat updates. Using `list.all()` directly from SQLAlchemy scalar responses creates lists.
**Action:** When querying a list of UUIDs (e.g. `scalars().all()`) and checking for presence within a loop, always convert the list to a `set` first (e.g. `set(dashes.scalars().all())`) to reduce lookup time from O(n) to O(1), making the loop O(n).
