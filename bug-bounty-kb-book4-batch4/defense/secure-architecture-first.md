# Secure Architecture First

- What it is: Security is cheapest and most effective when architectural risks are addressed before implementation.
- Where to look / how to identify it:
  - During design, map data flows, trust boundaries, authentication, storage, integrations, and high-value assets.
- Exploitation / test pattern:
  - Resolve structural security problems before code or customer dependencies make change expensive.
- Tools + exact CLI syntax (if mentioned):
  - Architecture diagrams + threat modeling.
- Common false-positive / WAF / edge-case notes:
  - Good architecture does not eliminate implementation bugs.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Require security review during architecture/design approval.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 20
