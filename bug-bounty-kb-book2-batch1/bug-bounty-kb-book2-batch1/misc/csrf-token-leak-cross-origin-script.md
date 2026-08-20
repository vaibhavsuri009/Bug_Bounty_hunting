# CSRF Token Leak Through Cross-Origin JavaScript

- What it is: A secret protected inside JSON may also be exposed in a JavaScript resource that browsers are allowed to load cross-origin.
- Where to look: Public JS/service-worker files containing user-specific URLs, tokens, nonces, or variables.
- Search loaded JavaScript for CSRF-token values also seen in authenticated requests or JSON responses.
- Determine whether an attacker page can include that script with a cross-origin `<script src>` tag.
- Generic pattern:
```html
<script src="https://target.example/user-specific-script.js"></script>
```
- Check whether the script creates a globally readable variable containing the token.
- If so, read that variable in the attacker page and use only a harmless test action to prove the token can bypass CSRF protection.
- Edge case: CORS protection on JSON does not automatically protect a script resource loaded via `<script src>`.
- False-positive trap: Static/public non-secret values are not meaningful token leaks.
- Remediation: Never place per-user CSRF secrets in cross-origin-loadable script resources or global variables.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 4
