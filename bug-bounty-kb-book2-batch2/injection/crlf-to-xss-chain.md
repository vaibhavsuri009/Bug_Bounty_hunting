# CRLF-to-XSS Response Chain

- What it is: Header injection is escalated by changing the response type and injecting HTML that executes script.
- Prerequisite: CRLF injection must allow attacker-controlled response headers/content.
- The book's example injects an HTML content type and then markup after line breaks.
```text
Content-Type: text/html
...
<svg onload=alert(document.domain)>
```
- For authorized testing, use a benign `alert(document.domain)` proof rather than cookie exfiltration.
- Confirm the JavaScript runs in the vulnerable application's origin.
- False positive: script running in a sandboxed/foreign origin does not demonstrate access to the target origin.
- Edge case: CSP, response parsing, duplicate headers, or browser normalization may block execution.
- Treat CRLF and XSS as separate primitives and document the exact chain.
- Remediation: prevent CR/LF header injection and apply CSP/output encoding as defense in depth.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 6
