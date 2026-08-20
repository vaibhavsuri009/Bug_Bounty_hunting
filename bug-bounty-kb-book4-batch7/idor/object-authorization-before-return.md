# Object Authorization Before Return

- What it is: IDOR is best prevented by authorizing access to each requested object before returning or modifying it.
- Where to look / how to identify it:
  - Review object/file retrieval routes that accept identifiers in paths, queries, headers, or request bodies.
- Exploitation / test pattern:
  - Resolve the object, then verify the authenticated user has permission to that exact object.
- Tools + exact CLI syntax (if mentioned):
  - Server-side authorization middleware/service.
- Common false-positive / WAF / edge-case notes:
  - Random identifiers reduce guessing but do not replace authorization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Perform per-object access checks on every read/write/delete operation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 33
