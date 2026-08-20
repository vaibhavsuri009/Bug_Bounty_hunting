# Static Analysis Pipeline

- What it is: Static analysis examines source without executing it to flag common security patterns and coding mistakes.
- Where to look / how to identify it:
  - Run language-appropriate SAST on commits/branches and tune rules to application conventions.
- Exploitation / test pattern:
  - Prioritize findings involving user-controlled data, dangerous sinks, missing auth checks, and insecure regex.
- Tools + exact CLI syntax (if mentioned):
  - Book examples: Checkmarx, PMD, Bandit, Brakeman.
- Common false-positive / WAF / edge-case notes:
  - Static analysis can produce many false positives and struggles with dynamic languages/business logic.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Tune rules, suppress with justification, and combine SAST with runtime/manual testing.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
