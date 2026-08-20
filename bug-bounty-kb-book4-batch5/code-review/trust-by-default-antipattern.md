# Trust-by-Default Server Account Anti-Pattern

- What it is: Running all application modules under one broadly privileged OS/database account lets one vulnerability reach unrelated resources.
- Where to look / how to identify it:
  - Map which processes can write logs, files, database rows, execute tools, and read secrets.
- Exploitation / test pattern:
  - Verify independent modules use separate constrained identities wherever feasible.
- Tools + exact CLI syntax (if mentioned):
  - OS/database permissions review.
- Common false-positive / WAF / edge-case notes:
  - Small applications may share a process but can still enforce capability boundaries.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Separate service identities and use least privilege per module.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
