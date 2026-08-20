# XSS Bypass: Capitalization and Encoding

- What it is: Evade simplistic string filters by changing capitalization or generating blocked characters at runtime.
- Where to look: Filters that match literal strings such as `script` or reject quotes/special characters.
- Case-variation example:
```html
<scrIPT>alert(1)</scrIPT>
```
- If quotes are blocked, JavaScript can construct strings from character codes:
```javascript
String.fromCharCode(104,116,116,112,58,47,47)
```
- Use encoding only to test whether validation is canonicalization-aware; keep the final PoC minimal.
- Check the browser's final decoded/interpreted representation, not only the raw request.
- False-positive/edge note: A WAF bypass without executable output is not XSS.
- Remediation: Canonicalize input before validation and use context-aware output encoding instead of blocklists.

## Source: Bug Bounty Bootcamp, Ch. 6
