# Security-by-Design vs Feature-Time Security

- What it is: Applications that embed security into architecture before feature development tend to avoid repeated inconsistent controls.
- Where to look / how to identify it:
  - Look for reusable authorization, validation, encoding, and sanitization layers shared across many features.
- Exploitation / test pattern:
  - Compare old and new implementations of similar features for security consistency.
- Tools + exact CLI syntax (if mentioned):
  - Source review and multi-endpoint behavior comparison.
- Common false-positive / WAF / edge-case notes:
  - Centralization can create systemic risk if the shared control itself is flawed.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Design secure defaults centrally and protect them with regression tests.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 7
