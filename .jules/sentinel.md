## 2025-02-23 - XSS Vulnerability in dangerouslySetInnerHTML
**Vulnerability:** Found multiple instances where `dangerouslySetInnerHTML` was used directly with unescaped/unsanitized text or HTML variables (e.g., `item.title`, `news.teaser`, `xmlContent`, `step.description`, `highlightedText`). This allowed for Cross-Site Scripting (XSS).
**Learning:** These variables originated from user input or external data sources and were rendered blindly. The application has a dedicated HTML sanitizer in `~/lib/utils/sanitize` specifically meant to address this.
**Prevention:** Always wrap dynamically generated or external strings with `sanitizeHtml(...)` from `~/lib/utils/sanitize` when using `dangerouslySetInnerHTML`. Add a fallback like `content || ""` to prevent undefined errors.
