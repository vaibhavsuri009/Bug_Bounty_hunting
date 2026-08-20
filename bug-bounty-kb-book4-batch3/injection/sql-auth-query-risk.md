# Authentication Query Injection Risk

- What it is: Login code that concatenates username/password input into SQL may allow authentication logic to be altered.
- Where to look / how to identify it:
  - Inspect authentication endpoints and source for direct query interpolation.
- Exploitation / test pattern:
  - Validate with a synthetic test database or controlled account rather than bypassing real accounts.
- Tools + exact CLI syntax (if mentioned):
  - No special tool required; source review is strongest.
- Common false-positive / WAF / edge-case notes:
  - Modern frameworks may parameterize queries automatically.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use prepared statements and secure password hashing.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
