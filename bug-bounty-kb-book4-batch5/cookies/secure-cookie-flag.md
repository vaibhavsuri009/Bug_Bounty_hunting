# Secure Cookie Flag

- What it is: The Secure attribute prevents a sensitive cookie from being sent over unencrypted HTTP.
- Where to look / how to identify it:
  - Inspect session/authentication cookies in DevTools or intercepted test traffic.
- Exploitation / test pattern:
  - Verify a controlled HTTP request does not include the Secure cookie.
- Tools + exact CLI syntax (if mentioned):
  - `Set-Cookie: auth_token=...; Secure`
- Common false-positive / WAF / edge-case notes:
  - Secure does not prevent JavaScript access; HttpOnly is a separate control.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Set Secure on all authentication and sensitive cookies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
