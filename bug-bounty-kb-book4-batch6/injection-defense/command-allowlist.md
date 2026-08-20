# Server Command Allowlist

- What it is: When user input must select server-side operations, users should choose from a predefined set of vetted commands rather than arbitrary command strings.
- Where to look / how to identify it:
  - Audit endpoints that accept command names, task types, operation names, or script actions.
- Exploitation / test pattern:
  - Validate allowed command, parameter schema, order, and frequency before invoking internal functionality.
- Tools + exact CLI syntax (if mentioned):
  - Server-side allowlist.
- Common false-positive / WAF / edge-case notes:
  - Allowlisting command names alone may not protect unsafe parameters or malicious sequencing.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Map user actions to safe internal functions instead of exposing a generic CLI.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 31
