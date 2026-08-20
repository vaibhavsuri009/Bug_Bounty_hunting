# Archetype + Business Logic Review

- What it is: Security review must look for standard vulnerability classes and feature-specific business-rule violations.
- Where to look / how to identify it:
  - Understand users, feature purpose, permissions, and business impact before reviewing implementation.
- Exploitation / test pattern:
  - Ask both 'is this XSS/CSRF/injection-prone?' and 'can a valid request break the intended business rule?'
- Tools + exact CLI syntax (if mentioned):
  - Code review + feature spec/threat model.
- Common false-positive / WAF / edge-case notes:
  - Automated scanners mainly cover archetypal issues and miss deep logic context.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Pair security reviewers with product/feature owners for high-risk changes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
