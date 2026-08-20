# Regression Test Required on Closure

- What it is: Every closed security issue should leave behind a regression test that prevents the same vulnerability from reappearing.
- Where to look / how to identify it:
  - Capture the secure invariant or minimal reproduction case from the fixed vulnerability.
- Exploitation / test pattern:
  - Fail CI if future changes reintroduce the vulnerable behavior.
- Tools + exact CLI syntax (if mentioned):
  - Any unit/integration/security test framework.
- Common false-positive / WAF / edge-case notes:
  - Testing one literal payload is weaker than testing the underlying security invariant.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Require regression coverage as a condition for security-ticket closure.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 27
