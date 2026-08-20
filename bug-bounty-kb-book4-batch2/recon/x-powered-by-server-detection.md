# Server Detection via Response Headers

- What it is: Default server headers can expose backend frameworks and exact versions.
- Where to look / how to identify it:
  - Inspect responses for `X-Powered-By`, `Server`, and framework-specific version headers.
- Exploitation / test pattern:
  - Cross-reference identified versions with public advisories during authorized assessment.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network → Headers.
- Common false-positive / WAF / edge-case notes:
  - Headers can be removed, proxied, or intentionally altered; treat them as evidence, not certainty.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable unnecessary version banners and framework disclosure headers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
