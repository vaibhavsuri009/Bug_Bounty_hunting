# Branch vs Fork Integration Risk

- What it is: Branching and forking OSS create different update and review risks that can affect security posture.
- Where to look / how to identify it:
  - Identify whether production code tracks upstream branches directly or uses a separated fork.
- Exploitation / test pattern:
  - Assess how upstream changes are reviewed before they reach production.
- Tools + exact CLI syntax (if mentioned):
  - Git repository history and branch/fork metadata.
- Common false-positive / WAF / edge-case notes:
  - A fork can also become stale and miss security fixes; separation is not automatically safer.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use controlled update workflows, code review, signed commits, and dependency monitoring.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
