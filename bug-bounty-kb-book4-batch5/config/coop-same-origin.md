# COOP `same-origin`

- What it is: Cross-Origin-Opener-Policy can isolate a page's browsing context from cross-origin opener relationships.
- Where to look / how to identify it:
  - Inspect security headers on pages that open or are opened by external sites.
- Exploitation / test pattern:
  - Use benign controlled new-tab tests to verify cross-origin opener references are unavailable.
- Tools + exact CLI syntax (if mentioned):
  - `Cross-Origin-Opener-Policy: same-origin`
- Common false-positive / WAF / edge-case notes:
  - Apps relying on cross-origin popup communication may require a different configuration.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use the strictest COOP mode compatible with legitimate workflows.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
