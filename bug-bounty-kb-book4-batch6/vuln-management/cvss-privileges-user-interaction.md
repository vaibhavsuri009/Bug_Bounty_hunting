# CVSS Privileges + User Interaction

- What it is: Privileges Required and User Interaction describe whether exploitation needs prior authorization or victim participation.
- Where to look / how to identify it:
  - Record whether the attacker must be unauthenticated, normal user, admin, or must induce another user action.
- Exploitation / test pattern:
  - Score based on the demonstrated exploit path, not an imagined worst-case route.
- Tools + exact CLI syntax (if mentioned):
  - CVSS calculator.
- Common false-positive / WAF / edge-case notes:
  - Social engineering-heavy variants may differ from the technical root cause being scored.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Track privilege and interaction changes if a later exploit chain lowers prerequisites.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
