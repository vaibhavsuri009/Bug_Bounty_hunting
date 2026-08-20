# Client-to-Server Security Review Path

- What it is: Starting code review from user-facing client actions helps prioritize reachable and business-critical server functionality.
- Where to look / how to identify it:
  - Review client code, map API calls, trace those APIs server-side, then follow helpers, databases, logs, uploads, and dependencies.
- Exploitation / test pattern:
  - After reachable paths, inspect exposed-but-unused APIs and then the remainder of the codebase.
- Tools + exact CLI syntax (if mentioned):
  - Source tree + API map.
- Common false-positive / WAF / edge-case notes:
  - Some critical server-only workflows may not have a client entry point.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Combine reachability-based review with asset/risk-based review.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
