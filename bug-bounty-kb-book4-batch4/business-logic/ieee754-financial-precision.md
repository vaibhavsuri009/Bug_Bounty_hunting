# IEEE754 Financial Precision Risk

- What it is: Binary floating-point can introduce small precision errors that become significant in repeated or compounded financial calculations.
- Where to look / how to identify it:
  - Identify money/reward calculations implemented with native floating-point types.
- Exploitation / test pattern:
  - Reproduce rounding behavior locally with representative values before assessing business impact.
- Tools + exact CLI syntax (if mentioned):
  - JavaScript console example: `0.1 + 0.2`.
- Common false-positive / WAF / edge-case notes:
  - Minor floating-point error is expected and usually harmless unless accumulated or misrounded.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use fixed-point/decimal money types and explicit rounding rules.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 18
