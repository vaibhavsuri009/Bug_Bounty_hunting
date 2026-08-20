# `X-Content-Type-Options: nosniff`

- What it is: `nosniff` prevents browsers from guessing a MIME type that differs from the server-declared content type.
- Where to look / how to identify it:
  - Inspect responses serving uploads, scripts, styles, and user-controlled files.
- Exploitation / test pattern:
  - Verify a harmless mismatched content type is not executed as a script in a test environment.
- Tools + exact CLI syntax (if mentioned):
  - `X-Content-Type-Options: nosniff`
- Common false-positive / WAF / edge-case notes:
  - Correct Content-Type is still required; nosniff does not fix an incorrectly declared executable type.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Send accurate MIME types and enable `nosniff` globally where compatible.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
