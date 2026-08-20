# HttpOnly Cookie Flag

- What it is: HttpOnly prevents JavaScript from reading a cookie, reducing session-token theft through XSS.
- Where to look / how to identify it:
  - Inspect session cookies for the HttpOnly flag and compare with `document.cookie` in a test account.
- Exploitation / test pattern:
  - Verify the sensitive cookie is absent from JavaScript-accessible cookie output.
- Tools + exact CLI syntax (if mentioned):
  - `Set-Cookie: ...; HttpOnly`
- Common false-positive / WAF / edge-case notes:
  - HttpOnly does not stop XSS from making authenticated requests on the user's behalf.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Mark session cookies HttpOnly and still prevent XSS at the root cause.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
