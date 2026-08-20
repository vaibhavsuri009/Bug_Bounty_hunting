# Unauthenticated User Data Exposure

- What it is: An API may expose private user data without requiring authentication or without honoring privacy settings.
- Where to look / how to identify it:
  - Test a controlled public/private account and compare whether the same endpoint returns sensitive fields when unauthenticated.
- Exploitation / test pattern:
  - Check user-search, detail, and GraphQL functions for consistent authentication and privacy enforcement.
- Tools + exact CLI syntax (if mentioned):
  - No special tool is required; use a raw HTTP client or Postman.
- Common false-positive / WAF / edge-case notes:
  - Public profile fields may be intentionally exposed; focus on fields expected to remain private.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Require authentication where appropriate and enforce privacy/authorization at every data resolver.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
