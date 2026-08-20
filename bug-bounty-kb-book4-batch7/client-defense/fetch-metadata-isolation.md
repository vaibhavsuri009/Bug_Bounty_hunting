# Fetch Metadata Isolation Policy

- What it is: Fetch Metadata headers tell the server request site, mode, destination, and user-initiation context.
- Where to look / how to identify it:
  - Inspect `Sec-Fetch-Site`, `Sec-Fetch-Mode`, `Sec-Fetch-Dest`, and `Sec-Fetch-User` on modern browsers.
- Exploitation / test pattern:
  - Use them to reject cross-site framing or other unexpected request contexts.
- Tools + exact CLI syntax (if mentioned):
  - Server middleware using Sec-Fetch-* headers.
- Common false-positive / WAF / edge-case notes:
  - Browser support varies; do not use as the sole defense.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use Fetch Metadata as defense-in-depth beside CSP, CSRF, and authorization controls.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
