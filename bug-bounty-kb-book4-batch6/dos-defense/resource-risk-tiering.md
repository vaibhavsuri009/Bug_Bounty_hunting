# DoS Resource Risk Tiering

- What it is: DoS exposure is better treated as a spectrum of resource cost than a simple vulnerable/secure state.
- Where to look / how to identify it:
  - Classify endpoints/jobs by CPU, memory, database, disk, network, and client-side cost.
- Exploitation / test pattern:
  - Prioritize high-cost functionality for limits, asynchronous execution, and abuse monitoring.
- Tools + exact CLI syntax (if mentioned):
  - Performance profiling/APM.
- Common false-positive / WAF / edge-case notes:
  - Slow operations can be acceptable when infrequent and protected.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use per-operation budgets, quotas, concurrency controls, and timeouts.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 32
