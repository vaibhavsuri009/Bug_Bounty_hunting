# Remove Eval-Like Code Paths

- What it is: String-to-code execution functions dramatically increase XSS and injection risk.
- Where to look / how to identify it:
  - Search for `eval`, string-form timers, Function constructors, and similar interpreters.
- Exploitation / test pattern:
  - Refactor APIs to accept structured parameters and executable callbacks rather than code strings.
- Tools + exact CLI syntax (if mentioned):
  - Static analysis/source search.
- Common false-positive / WAF / edge-case notes:
  - CSP can block eval-like execution, but secure code should not rely on CSP alone.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Remove eval-like patterns and use narrowly typed functions.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
