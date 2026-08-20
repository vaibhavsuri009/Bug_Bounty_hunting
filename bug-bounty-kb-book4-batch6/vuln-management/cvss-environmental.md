# CVSS Environmental Scoring

- What it is: Environmental scoring adapts vulnerability severity to the affected organization's actual confidentiality, integrity, and availability requirements.
- Where to look / how to identify it:
  - Determine how critical the application and affected data are to the specific environment.
- Exploitation / test pattern:
  - Use business contracts, uptime commitments, regulatory requirements, and asset classification to modify impact.
- Tools + exact CLI syntax (if mentioned):
  - CVSS environmental calculator.
- Common false-positive / WAF / edge-case notes:
  - A public demo app and a regulated financial system can have very different environmental risk for the same flaw.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain asset criticality metadata so environmental scoring is repeatable.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
