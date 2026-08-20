# Weakest-Link Layer Analysis

- What it is: A feature can remain vulnerable if one of several data-processing layers omits security controls.
- Where to look / how to identify it:
  - Trace attacker-controlled data across API POST, database write/read, API GET, and client render stages.
- Exploitation / test pattern:
  - Mark every layer where the same attack class could be prevented or reintroduced.
- Tools + exact CLI syntax (if mentioned):
  - Architecture/data-flow mapping.
- Common false-positive / WAF / edge-case notes:
  - Duplicating identical filters may not provide true defense in depth.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use independent controls at ingestion, storage, retrieval, and rendering boundaries.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 7
