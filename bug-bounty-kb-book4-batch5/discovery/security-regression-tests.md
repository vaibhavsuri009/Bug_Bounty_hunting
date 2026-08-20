# Security Regression Test Suite

- What it is: Regression tests encode the expected secure behavior after a vulnerability is fixed so later changes cannot silently reopen it.
- Where to look / how to identify it:
  - Convert each root cause into a deterministic test with both failing and passing conditions.
- Exploitation / test pattern:
  - Run on commit/push when practical, otherwise on a regular schedule.
- Tools + exact CLI syntax (if mentioned):
  - Any normal unit/integration framework; book example uses Jest.
- Common false-positive / WAF / edge-case notes:
  - A test matching only one payload may miss variants of the same root cause.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Test invariants/root causes and require passing security regressions before merge.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
