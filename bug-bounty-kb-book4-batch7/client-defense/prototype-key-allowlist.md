# Prototype Pollution Key Sanitization

- What it is: Prototype pollution can be blocked by rejecting dangerous or unexpected object keys before merge/update operations.
- Where to look / how to identify it:
  - Inspect recursive merges and user-controlled JSON/object updates.
- Exploitation / test pattern:
  - Allowlist accepted keys and explicitly block prototype-related paths.
- Tools + exact CLI syntax (if mentioned):
  - JavaScript object validation.
- Common false-positive / WAF / edge-case notes:
  - Flexible-schema apps may need a more dynamic validation model than a static key list.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate keys deeply and reject `__proto__`, constructor/prototype paths, and equivalents.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
