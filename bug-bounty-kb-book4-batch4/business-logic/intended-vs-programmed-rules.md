# Intended vs Programmed Business Rules

- What it is: Business logic vulnerabilities occur when programmed rules permit an outcome the business did not intend.
- Where to look / how to identify it:
  - Document the intended business process and compare it with the exact API/state transitions the application allows.
- Exploitation / test pattern:
  - Search for valid-but-abusive sequences that remain within normal request syntax.
- Tools + exact CLI syntax (if mentioned):
  - Workflow mapping and multi-step request analysis.
- Common false-positive / WAF / edge-case notes:
  - Unexpected behavior is not necessarily a security issue unless it violates a meaningful business rule.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Translate business requirements into explicit server-side validations and abuse-case tests.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
