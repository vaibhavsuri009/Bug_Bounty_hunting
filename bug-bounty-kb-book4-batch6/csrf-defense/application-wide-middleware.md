# Application-Wide Anti-CSRF Middleware

- What it is: Central middleware reduces the chance that one route forgets origin/token validation.
- Where to look / how to identify it:
  - Place CSRF checks before route/business logic and apply them consistently to protected requests.
- Exploitation / test pattern:
  - Validate origin/referrer and token, log failures, and stop execution before state changes.
- Tools + exact CLI syntax (if mentioned):
  - Server middleware.
- Common false-positive / WAF / edge-case notes:
  - Route exclusions can become weak links and must be explicitly reviewed.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize CSRF enforcement and maintain a small audited exception list.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 29
