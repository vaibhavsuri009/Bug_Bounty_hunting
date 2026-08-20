# Permanent vs Partial Security Fix

- What it is: A vulnerability should preferably be resolved across the full affected surface rather than patched only at the reported endpoint.
- Where to look / how to identify it:
  - Search for equivalent code paths, endpoints, methods, clients, and duplicated vulnerable patterns.
- Exploitation / test pattern:
  - If a full fix cannot ship immediately, deploy a temporary mitigation and open a separate tracked issue for remaining exposure.
- Tools + exact CLI syntax (if mentioned):
  - Source search + vulnerability ticketing.
- Common false-positive / WAF / edge-case notes:
  - Closing a ticket after a narrow patch can hide still-vulnerable variants.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Track root-cause remediation and keep partial-fix follow-ups open with their own severity.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
