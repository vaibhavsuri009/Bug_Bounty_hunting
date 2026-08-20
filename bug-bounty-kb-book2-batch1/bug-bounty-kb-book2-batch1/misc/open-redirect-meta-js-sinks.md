# Open Redirect via Meta Refresh or JavaScript

- What it is: Redirect behavior can be driven by HTML or DOM sinks rather than an HTTP `Location` header.
- Where to look: User-controlled values inserted into `<meta http-equiv="refresh">` or JavaScript location properties.
- Meta-refresh pattern:
```html
<meta http-equiv="refresh" content="0; url=https://attacker.example/">
```
- JavaScript redirect sinks to watch:
```javascript
window.location = "https://attacker.example/"
window.location.href = "https://attacker.example/"
window.location.replace("https://attacker.example/")
```
- Trace whether URL parameters or other attacker input reaches these sinks.
- Confirm navigation occurs without an effective destination allowlist.
- False-positive trap: Merely finding these APIs is not a bug if the destination cannot be influenced by an attacker.
- Remediation: Keep redirect targets server-controlled or validate them against a strict allowlist.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 2
