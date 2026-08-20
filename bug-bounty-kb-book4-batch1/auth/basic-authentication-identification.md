# HTTP Basic Authentication Identification

- What it is: HTTP Basic authentication places base64-encoded `username:password` credentials in the Authorization header.
- Where to look / how to identify it:
  - Look for `Authorization: Basic ...` in requests and verify that transport encryption is used.
- Exploitation / test pattern:
  - Decode only credentials belonging to an authorized test account to understand request format.
- Tools + exact CLI syntax (if mentioned):
  - Local decode example: `echo 'BASE64' | base64 -d`.
- Common false-positive / WAF / edge-case notes:
  - Base64 is encoding rather than encryption; HTTPS is essential.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer stronger authentication where practical, require TLS, rate-limit attempts, and avoid credential reuse.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
