# ReDoS Catastrophic Backtracking

- What it is: Certain nested or ambiguous regular expressions can consume exponentially increasing CPU time on crafted nonmatching inputs.
- Where to look / how to identify it:
  - Review user-reachable regex validation and benchmark suspicious patterns in a local test environment.
- Exploitation / test pattern:
  - Increase controlled input length gradually and measure execution time; stop before system degradation.
- Tools + exact CLI syntax (if mentioned):
  - Local regex test harness and timing measurements.
- Common false-positive / WAF / edge-case notes:
  - DoS testing is usually prohibited on live bug bounty targets; use isolated environments.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use linear-time regex engines/patterns, input length limits, and regex linting.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 14
