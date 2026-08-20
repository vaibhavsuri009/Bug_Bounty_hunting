# Local Storage Sensitive Data Review

- What it is: Browser local storage persists key/value state across sessions and is readable by JavaScript from the same origin.
- Where to look / how to identify it:
  - Inspect local storage for authentication tokens, secrets, PII, privileged flags, or other data that should not persist client-side.
- Exploitation / test pattern:
  - Compare stored values before/after authentication and logout using authorized accounts.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Application/Storage panel.
- Common false-positive / WAF / edge-case notes:
  - Client-visible configuration is often intentional; focus on secrets and security decisions.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Avoid storing reusable secrets client-side and clear sensitive state on logout or expiry.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
