# Security Code Review Four-Question Baseline

- What it is: A compact security review can begin by tracing how data moves, is stored, is presented, and is processed.
- Where to look / how to identify it:
  - Ask: how is data transmitted; how is it stored; how is it presented to the client; what happens server-side.
- Exploitation / test pattern:
  - Use these questions on every security-relevant commit as a first-pass review.
- Tools + exact CLI syntax (if mentioned):
  - Code review/VCS diff.
- Common false-positive / WAF / edge-case notes:
  - This baseline will miss nuanced vulnerability classes and should not replace specialized review.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Add security review checklists and domain-specific reviewers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 20
