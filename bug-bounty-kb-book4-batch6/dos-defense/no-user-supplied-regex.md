# Reject User-Supplied Regex

- What it is: Allowing arbitrary user-defined regex gives clients a direct way to create excessive CPU consumption.
- Where to look / how to identify it:
  - Identify search/filter APIs that accept raw regular expressions.
- Exploitation / test pattern:
  - Replace raw regex input with constrained filters or a safe query language.
- Tools + exact CLI syntax (if mentioned):
  - API schema review.
- Common false-positive / WAF / edge-case notes:
  - Some expert tools legitimately need regex; isolate and heavily limit them.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use fixed patterns, safe-regex engines, timeouts, and strict input limits.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 32
