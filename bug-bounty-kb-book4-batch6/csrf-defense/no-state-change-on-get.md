# No State Changes on GET

- What it is: GET routes are broadly triggerable by links and embedded resources, making them unsuitable for state-changing actions.
- Where to look / how to identify it:
  - Audit all GET endpoints for writes, updates, deletes, transfers, emails, or privilege changes.
- Exploitation / test pattern:
  - Split read behavior into GET and mutation behavior into POST/PUT/PATCH/DELETE.
- Tools + exact CLI syntax (if mentioned):
  - Route inventory/static analysis.
- Common false-positive / WAF / edge-case notes:
  - Changing the verb alone does not fully eliminate CSRF risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use safe HTTP semantics plus CSRF middleware on all state-changing methods.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 29
