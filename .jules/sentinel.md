## 2025-02-14 - XSS in React dangerouslySetInnerHTML
**Vulnerability:** External news/API content (titles, text, highlighted search results) were being rendered directly using React's `dangerouslySetInnerHTML` without proper sanitization.
**Learning:** This existed because the content required HTML formatting (e.g. bolding, line breaks, search highlighting), but untrusted external content and generated HTML fragments weren't sanitized before injection.
**Prevention:** Always use `sanitizeHtml` from `~/lib/utils/sanitize` when using `dangerouslySetInnerHTML` with dynamic content, especially from third-party APIs or search inputs.
