# Iframe GET CSRF

- What it is: An iframe `src` automatically loads its target, which can trigger a vulnerable state-changing GET request.
- Where to look / how to identify it:
  - Check whether sensitive GET endpoints can be framed and invoked from another page.
- Exploitation / test pattern:
  - Confirm only with a benign controlled change in a test account.
- Tools + exact CLI syntax (if mentioned):
  - Relevant pattern: `<iframe src='https://target/...'></iframe>`.
- Common false-positive / WAF / edge-case notes:
  - Iframe protections may block rendering but not always the underlying request.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use POST/PUT/PATCH for state changes, SameSite cookies, and server-side CSRF validation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
