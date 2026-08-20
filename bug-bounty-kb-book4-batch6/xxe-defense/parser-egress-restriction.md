# XML Parser Egress Restriction

- What it is: Even if parser configuration fails, restricting filesystem/network access can reduce XXE escalation impact.
- Where to look / how to identify it:
  - Map the parser process permissions and outbound network destinations.
- Exploitation / test pattern:
  - Ensure the parser cannot access sensitive files or arbitrary external/internal hosts.
- Tools + exact CLI syntax (if mentioned):
  - OS sandboxing, firewall/egress policy, container permissions.
- Common false-positive / WAF / edge-case notes:
  - Least privilege reduces impact but does not remove the underlying parser flaw.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Combine hardened parser settings with filesystem and network isolation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 30
