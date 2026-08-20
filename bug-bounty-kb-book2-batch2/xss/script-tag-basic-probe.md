# Basic Script-Tag XSS Probe

- What it is: Unsanitized HTML special characters let attacker input become executable JavaScript.
- Look for reflected or stored inputs containing `"`, `'`, `<`, or `>`.
- Start with a minimal origin-confirmation payload.
```html
<script>alert(document.domain)</script>
```
- Inspect page source to verify whether the payload is emitted as markup or encoded entities.
- If `<` becomes `&lt;`, this exact vector is neutralized; test the actual surrounding context instead.
- Confirm execution in the expected origin, not merely that a popup appears.
- False positive: execution in a sandboxed iframe or unrelated origin may have little/no target impact.
- Edge case: CSP can block inline `<script>` while other event-handler contexts remain reachable.
- Remediation: contextually encode user data and enforce CSP as defense in depth.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
