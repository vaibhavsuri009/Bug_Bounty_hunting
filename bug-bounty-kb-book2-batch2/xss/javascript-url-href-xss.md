# `javascript:` URL in an `href` Sink

- What it is: User input controls a link destination and accepts the `javascript:` scheme.
- Look for URL parameters reflected into `<a href="...">`.
- Replace the expected URL with a harmless JavaScript-scheme probe.
```text
javascript:alert(document.domain)
```
- Trigger the link in more than one interaction path; the book's Google example differed between mouse click and keyboard activation.
- Confirm the JavaScript inherits the target page's origin.
- False positive: the browser may block `javascript:` navigation or execute it in a non-sensitive context.
- Edge case: event handlers such as `onmousedown` may sanitize only one activation path.
- No angle brackets are required, making this useful where HTML special characters are filtered.
- Remediation: allowlist safe URL schemes (`https`, optionally `http`) and canonicalize before validation.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
