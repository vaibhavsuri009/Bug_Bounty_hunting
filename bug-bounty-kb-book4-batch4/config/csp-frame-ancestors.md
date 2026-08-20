# CSP `frame-ancestors` Clickjacking Defense

- What it is: `frame-ancestors` controls which origins may embed a page and is a primary clickjacking defense.
- Where to look / how to identify it:
  - Inspect CSP on pages containing sensitive state-changing UI.
- Exploitation / test pattern:
  - Confirm untrusted origins cannot frame the page using a local harmless iframe test.
- Tools + exact CLI syntax (if mentioned):
  - Browser + CSP headers.
- Common false-positive / WAF / edge-case notes:
  - Frameability may be intentional for embeddable widgets.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use `frame-ancestors 'none'` or a strict allowlist for sensitive pages.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
