# CVSS Temporal Scoring

- What it is: Temporal scoring adjusts severity based on exploit maturity, remediation availability, and confidence in the report.
- Where to look / how to identify it:
  - Assess whether exploitation is theoretical, PoC, functional, or widespread; whether a fix/workaround exists; and how reliable the report is.
- Exploitation / test pattern:
  - Update the temporal score as exploits or mitigations mature.
- Tools + exact CLI syntax (if mentioned):
  - CVSS temporal calculator.
- Common false-positive / WAF / edge-case notes:
  - Temporal score changes over time and should not be stored as a one-time permanent value.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Re-score important vulnerabilities when public exploits or official fixes become available.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
