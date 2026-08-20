# Regex DoS Linting

- What it is: Catastrophic-backtracking regex patterns can be detected before release through static rules or performance testing.
- Where to look / how to identify it:
  - Search for nested greedy/repeated groups and any regex applied to untrusted strings.
- Exploitation / test pattern:
  - Run regex-lint/performance tests against representative long inputs in CI.
- Tools + exact CLI syntax (if mentioned):
  - Regex linter/performance tester.
- Common false-positive / WAF / edge-case notes:
  - Many complex regexes are safe; static rules can produce false positives.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer linear-time patterns, bound input lengths, and block user-supplied regex.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 32
