# Production-Like Vulnerability Reproduction

- What it is: Every reported vulnerability should be reproduced in a production-like staging environment before remediation begins.
- Where to look / how to identify it:
  - Maintain staging with representative mock users, objects, integrations, and production-equivalent configuration.
- Exploitation / test pattern:
  - Reproduce using safe test data, log the result, and determine the root cause before paying bounties or assigning engineering work.
- Tools + exact CLI syntax (if mentioned):
  - Automated staging deployment plus the original report/PoC.
- Common false-positive / WAF / edge-case notes:
  - User misconfiguration and product behavior can resemble vulnerabilities; reproduction separates false positives from valid issues.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Automate staging parity and require reproduction evidence in the triage workflow.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
