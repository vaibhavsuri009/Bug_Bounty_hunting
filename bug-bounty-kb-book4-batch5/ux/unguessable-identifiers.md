# Avoid Guessable Identifiers

- What it is: Predictable user/resource identifiers make enumeration easier even when direct access is restricted.
- Where to look / how to identify it:
  - Review numeric sequential IDs, signup-time-derived IDs, and obvious path naming.
- Exploitation / test pattern:
  - Use controlled records to determine whether identifiers follow an easily guessed sequence.
- Tools + exact CLI syntax (if mentioned):
  - Traffic/response observation.
- Common false-positive / WAF / edge-case notes:
  - Opaque IDs are defense-in-depth, not a substitute for authorization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use random/opaque identifiers where practical and enforce authorization on every object.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 23
