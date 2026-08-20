# Primary-Key Database Detection

- What it is: Different database engines use recognizable default primary-key generation schemes.
- Where to look / how to identify it:
  - Collect several object identifiers from paths, query parameters, request bodies, and response metadata.
- Exploitation / test pattern:
  - Compare patterns against documented key-generation algorithms for likely database technologies.
- Tools + exact CLI syntax (if mentioned):
  - Manual traffic analysis and public database documentation.
- Common false-positive / WAF / edge-case notes:
  - Sequential or custom IDs may match many systems and require secondary evidence.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use opaque identifiers when appropriate, but always enforce authorization independently.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 6
