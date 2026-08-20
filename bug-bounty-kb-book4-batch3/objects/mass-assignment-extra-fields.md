# Mass Assignment via Extra Object Fields

- What it is: Mass assignment occurs when an API blindly writes all client-supplied object keys to persistent state.
- Where to look / how to identify it:
  - Prioritize profile updates, dynamic forms, game/user state, registration, and administrative object updates.
- Exploitation / test pattern:
  - Add one harmless unauthorized field to a controlled object and check whether it persists.
- Tools + exact CLI syntax (if mentioned):
  - Proxy/Postman or direct API request editing.
- Common false-positive / WAF / edge-case notes:
  - Unknown fields may be ignored, which is secure behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Allowlist writable fields and use explicit DTO/schema mapping.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 15
