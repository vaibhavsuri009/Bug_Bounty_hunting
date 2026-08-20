# Stored XSS Across Secondary Render Locations

- What it is: A payload is safely displayed at submission time but later rendered unsafely somewhere else.
- Look for values reused across profiles, admin panels, social channels, emails, previews, or exports.
- Store a benign unique marker or safe XSS probe in an editable field.
- Visit every feature that consumes the same data.
```html
"><img src=x onerror=alert(document.domain)>
```
- The book's Shopify example executed only in a secondary sales-channel view.
- Record which role/user renders the payload and whether execution crosses privilege boundaries.
- False positive: a payload stored successfully but encoded at every render sink is not XSS.
- Edge case: execution may require another workflow step or higher-privileged viewer.
- Remediation: encode on output at every rendering sink, not only when data is first submitted.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 7
