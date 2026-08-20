# User-Supplied CSS Risk

- What it is: User-controlled CSS can leak page state through resource-loading features and complex selectors even without JavaScript.
- Where to look / how to identify it:
  - Review profile themes, custom stylesheets, CSS editors, and any CSS loaded from user-controlled data.
- Exploitation / test pattern:
  - Prefer server-generated styles from a limited set of safe properties rather than arbitrary uploaded CSS.
- Tools + exact CLI syntax (if mentioned):
  - CSS parser/allowlist and CSP.
- Common false-positive / WAF / edge-case notes:
  - CSS capability differs across browsers and evolves; full sanitization is difficult.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disallow arbitrary CSS or allowlist non-networking, non-executable style properties.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
