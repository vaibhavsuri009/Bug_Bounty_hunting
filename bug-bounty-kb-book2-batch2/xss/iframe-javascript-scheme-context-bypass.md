# Iframe `javascript:` Scheme Context Bypass

- What it is: An iframe is created in the target DOM and its `src` uses JavaScript that executes with inherited origin.
- Prerequisite: attacker input must be able to write an iframe into the target document.
- The book's proof pattern is:
```html
<iframe src="javascript:alert(document.domain)"></iframe>
```
- Confirm the alert reports the vulnerable site's domain.
- This can bypass page-level JavaScript wrappers when the newly created iframe lacks the same defensive script state.
- False positive: execution in a sandboxed/opaque origin is not equivalent to target-origin XSS.
- Edge case: CSP `script-src`, `frame-src`, sandbox attributes, and browser changes may block the technique.
- Keep proof limited to origin confirmation.
- Remediation: fix the upstream injection and enforce CSP/sandboxing as defense in depth.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
