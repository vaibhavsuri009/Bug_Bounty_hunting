# CSP `default-src` Baseline

- What it is: `default-src` acts as a fallback source allowlist for resource types without a more specific directive.
- Where to look / how to identify it:
  - Review whether sensitive pages define a restrictive default source such as `'self'` or `'none'` where appropriate.
- Exploitation / test pattern:
  - Use CSP report-only mode first when tightening an existing application.
- Tools + exact CLI syntax (if mentioned):
  - Browser console/CSP reporting.
- Common false-positive / WAF / edge-case notes:
  - A restrictive default can break legitimate resources if dependencies are not mapped.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Start restrictive and explicitly add required origins per directive.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
