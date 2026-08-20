# Network Timing Side-Channel Signal

- What it is: Request timing can reveal different server-side execution paths even when response bodies look identical.
- Where to look / how to identify it:
  - Create a baseline from equivalent requests and compare queue, waiting, download, and total timings.
- Exploitation / test pattern:
  - Treat repeatable timing differences as a clue for later controlled side-channel validation.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network → Timing.
- Common false-positive / WAF / edge-case notes:
  - Network jitter creates false positives; repeat tests and compare statistically.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Normalize externally observable behavior where practical and avoid secret-dependent processing differences.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
