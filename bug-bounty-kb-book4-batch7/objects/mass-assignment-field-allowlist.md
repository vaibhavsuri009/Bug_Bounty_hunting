# Mass Assignment Field Allowlist

- What it is: Mass assignment can be prevented by accepting only a predefined set of client-writable object fields.
- Where to look / how to identify it:
  - Identify API endpoints that update objects using entire client-supplied JSON/body objects.
- Exploitation / test pattern:
  - Create an explicit writable-field list and reject or discard all other keys before database update.
- Tools + exact CLI syntax (if mentioned):
  - Server-side schema/validation code.
- Common false-positive / WAF / edge-case notes:
  - Client-side form restrictions do not prevent direct API manipulation.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use server-side allowlists for writable fields and apply them before persistence.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 33
