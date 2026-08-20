# CSP `unsafe-inline` / `unsafe-eval` Risk

- What it is: Enabling `'unsafe-inline'` or `'unsafe-eval'` weakens CSP by re-enabling major XSS execution paths.
- Where to look / how to identify it:
  - Search `script-src` and related directives for these keywords.
- Exploitation / test pattern:
  - Assess whether the application can migrate to nonce/hash-based execution.
- Tools + exact CLI syntax (if mentioned):
  - CSP header review.
- Common false-positive / WAF / edge-case notes:
  - Legacy frameworks may require unsafe settings temporarily.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Remove unsafe directives and migrate to nonce/hash/strict-dynamic patterns.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
