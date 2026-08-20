# Bug Bounty as Discovery Layer

- What it is: Bug bounty programs add financial incentives and external researcher diversity on top of responsible disclosure.
- Where to look / how to identify it:
  - Define eligible assets, vulnerability classes, severity/reward model, duplicates policy, and prohibited testing.
- Exploitation / test pattern:
  - Use a platform or internal triage workflow to track reports through remediation.
- Tools + exact CLI syntax (if mentioned):
  - HackerOne/Bugcrowd are examples from the source.
- Common false-positive / WAF / edge-case notes:
  - A bounty program without internal triage/remediation capacity can create backlog and risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Start with mature scope/response processes and expand gradually.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
