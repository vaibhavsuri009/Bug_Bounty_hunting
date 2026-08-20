# Feature Requirement Security Review

- What it is: Security architecture begins by translating business requirements into data, trust, and privilege risks before implementation.
- Where to look / how to identify it:
  - For each requirement, identify credentials, PII, financial data, roles, search, uploads, integrations, and external communication.
- Exploitation / test pattern:
  - Derive explicit security requirements from every business feature before selecting implementation details.
- Tools + exact CLI syntax (if mentioned):
  - Architecture/design review.
- Common false-positive / WAF / edge-case notes:
  - Requirements can change during development; security review must follow those changes.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Embed security stakeholders into product/design planning.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
