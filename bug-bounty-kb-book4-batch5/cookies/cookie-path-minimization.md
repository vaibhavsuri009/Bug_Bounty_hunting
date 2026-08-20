# Cookie Path Minimization

- What it is: The Path attribute limits which URL paths receive a cookie.
- Where to look / how to identify it:
  - Identify sensitive cookies used only by a subsection of an application.
- Exploitation / test pattern:
  - Verify requests outside the configured path do not include the cookie.
- Tools + exact CLI syntax (if mentioned):
  - `Set-Cookie: ...; Path=/account`
- Common false-positive / WAF / edge-case notes:
  - Path is not an authorization boundary and same-origin script risks may remain.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Set the narrowest practical cookie Path and enforce server-side authorization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
