# Private Package Mirror

- What it is: An organization-controlled package mirror reduces exposure to registry changes and dependency tampering.
- Where to look / how to identify it:
  - Consider for high-value production systems with large package ecosystems.
- Exploitation / test pattern:
  - Mirror approved artifacts and build production only from the controlled repository.
- Tools + exact CLI syntax (if mentioned):
  - Private npm/Maven/artifact registry.
- Common false-positive / WAF / edge-case notes:
  - Mirrors add operational overhead and can propagate compromised packages if ingestion is not verified.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Scan, sign, and approve artifacts before mirroring.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
