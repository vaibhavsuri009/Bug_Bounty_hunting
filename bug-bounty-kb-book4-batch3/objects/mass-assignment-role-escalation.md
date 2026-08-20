# Mass Assignment Role Escalation

- What it is: A dangerous mass-assignment case occurs when security-sensitive fields such as admin/role flags can be written by ordinary users.
- Where to look / how to identify it:
  - Search response objects/documentation for privileged fields absent from the normal edit UI.
- Exploitation / test pattern:
  - Use a controlled account and a harmless privilege marker in a lab; do not target real admin resources.
- Tools + exact CLI syntax (if mentioned):
  - Request replay and object comparison.
- Common false-positive / WAF / edge-case notes:
  - Client-visible role fields may be read-only despite being present in responses.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Separate read/write schemas and block privilege fields from untrusted updates.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 15
