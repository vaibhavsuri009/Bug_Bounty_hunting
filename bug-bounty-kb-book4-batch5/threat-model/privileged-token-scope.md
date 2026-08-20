# Privileged Token Scope Reduction

- What it is: Broad privileged tokens can turn a single credential compromise into full database or system compromise.
- Where to look / how to identify it:
  - Inventory admin/service tokens and map exact functions, tables, columns, and APIs each can access.
- Exploitation / test pattern:
  - Reduce permissions to the minimum required and separate read/write functions.
- Tools + exact CLI syntax (if mentioned):
  - IAM/database role review.
- Common false-positive / WAF / edge-case notes:
  - Operational convenience often leads to overprivilege.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use scoped short-lived tokens, least privilege, service identities, and independent audit logs.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
