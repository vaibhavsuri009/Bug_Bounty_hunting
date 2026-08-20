# CORP Resource Isolation

- What it is: Cross-Origin-Resource-Policy limits where browser resources can be read, adding protection against cross-origin leaks and side channels.
- Where to look / how to identify it:
  - Inspect resources containing sensitive data for CORP headers.
- Exploitation / test pattern:
  - Validate with controlled cross-origin embedding/fetch attempts.
- Tools + exact CLI syntax (if mentioned):
  - `Cross-Origin-Resource-Policy: same-origin`
- Common false-positive / WAF / edge-case notes:
  - `same-site` is weaker because related subdomains can still access resources.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use `same-origin` for sensitive resources unless cross-site sharing is explicitly required.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
