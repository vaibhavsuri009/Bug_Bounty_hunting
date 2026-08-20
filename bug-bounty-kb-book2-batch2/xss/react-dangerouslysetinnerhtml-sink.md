# React `dangerouslySetInnerHTML` Sink Review

- What it is: React normally escapes HTML, but `dangerouslySetInnerHTML` deliberately bypasses that protection.
- Look for React components that place server-provided or user-controlled HTML into this API.
- Search JavaScript/source bundles for `dangerouslySetInnerHTML`.
- Trace whether attacker-controlled Markdown, comments, profile text, or API data reaches the sink.
```jsx
<div dangerouslySetInnerHTML={{__html: value}} />
```
- Validate with a harmless HTML marker before attempting script execution.
- The book's HackerOne example became relevant because trusted server HTML was inserted directly into the DOM.
- False positive: the sink is not vulnerable when `value` is rigorously sanitized before assignment.
- Edge case: sanitization bugs may appear only with malformed attributes or unusual encodings.
- Tools: browser DevTools/source inspection.
- Remediation: avoid this API for untrusted content or sanitize with a robust allowlist-based HTML sanitizer.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
