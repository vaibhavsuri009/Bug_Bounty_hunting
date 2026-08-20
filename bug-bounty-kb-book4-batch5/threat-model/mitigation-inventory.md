# Threat Model Mitigation Inventory

- What it is: A useful threat model documents which controls already mitigate each identified attack vector.
- Where to look / how to identify it:
  - Map each threat to validation, prepared statements, authorization, logging, rate limits, query limits, or other controls.
- Exploitation / test pattern:
  - Verify the control actually covers the full vector before marking the risk mitigated.
- Tools + exact CLI syntax (if mentioned):
  - Mitigation table.
- Common false-positive / WAF / edge-case notes:
  - Listing a control without verifying implementation can create false assurance.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Link mitigations to code/config/tests and assign owners.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
