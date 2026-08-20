# Random Object Reference as Defense-in-Depth

- What it is: High-entropy object references make enumeration harder when direct object identifiers cannot be removed.
- Where to look / how to identify it:
  - Use random IDs for files/objects only in addition to authorization and rate limits.
- Exploitation / test pattern:
  - Measure identifier entropy and ensure predictable metadata is not embedded.
- Tools + exact CLI syntax (if mentioned):
  - UUID/secure random ID generator.
- Common false-positive / WAF / edge-case notes:
  - Opaque IDs alone do not prevent BOLA/IDOR if leaked or shared.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use random identifiers as defense-in-depth, not the primary access control.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 33
