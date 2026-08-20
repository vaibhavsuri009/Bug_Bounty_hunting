# Security Layer Count Prioritization

- What it is: Features protected at only one layer are often more attractive targets than features protected at several independent layers.
- Where to look / how to identify it:
  - Map where validation, authorization, sanitization, storage, retrieval, and client rendering controls occur.
- Exploitation / test pattern:
  - Prioritize features with many processing layers but few explicit security controls.
- Tools + exact CLI syntax (if mentioned):
  - Recon map and architecture notes.
- Common false-positive / WAF / edge-case notes:
  - More layers do not automatically mean secure; duplicated weak controls can still fail together.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply defense in depth at independent trust boundaries.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 7
