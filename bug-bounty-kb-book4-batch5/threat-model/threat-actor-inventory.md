# Threat Actor Inventory

- What it is: A threat model should include external users, authenticated users, admins, support staff, insiders, service accounts, and autonomous scripts.
- Where to look / how to identify it:
  - List each actor and the permissions/resources they can legitimately access.
- Exploitation / test pattern:
  - Rank what damage each actor could cause if malicious, compromised, or malfunctioning.
- Tools + exact CLI syntax (if mentioned):
  - Threat-actor table.
- Common false-positive / WAF / edge-case notes:
  - Focusing only on external human attackers misses major insider and machine risks.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Model human and machine identities separately and apply least privilege to both.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
