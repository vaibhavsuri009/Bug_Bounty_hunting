# Threat Model Logic Design

- What it is: Logic design documents what a feature is intended to do from a business/functionality perspective.
- Where to look / how to identify it:
  - Capture actors, allowed actions, ranges, workflows, state changes, and business constraints before technical details.
- Exploitation / test pattern:
  - Use the logic design to identify application-specific abuse cases such as out-of-range scores or unauthorized workflows.
- Tools + exact CLI syntax (if mentioned):
  - Threat-model document.
- Common false-positive / WAF / edge-case notes:
  - Logic descriptions that are too vague cannot expose business-rule gaps.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain clear business invariants and update them whenever feature behavior changes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
