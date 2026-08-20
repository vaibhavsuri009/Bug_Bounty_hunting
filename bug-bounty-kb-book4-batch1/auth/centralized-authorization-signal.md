# Centralized vs Per-Endpoint Authorization Signal

- What it is: Authorization implemented separately in every endpoint is more error-prone than centralized policy enforcement.
- Where to look / how to identify it:
  - During code or black-box analysis, compare access checks across similar endpoints and methods.
- Exploitation / test pattern:
  - Identify inconsistent behavior between endpoints handling the same resource or action.
- Tools + exact CLI syntax (if mentioned):
  - Multi-role test accounts plus request comparison.
- Common false-positive / WAF / edge-case notes:
  - Different endpoints may intentionally have different policies; confirm the intended model.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize access-control decisions and cover them with reusable policy tests.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
