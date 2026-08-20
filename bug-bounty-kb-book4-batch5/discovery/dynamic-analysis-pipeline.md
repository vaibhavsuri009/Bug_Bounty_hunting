# Dynamic Analysis Pipeline

- What it is: Dynamic analysis evaluates an executing application and can confirm issues that are difficult to reason about statically.
- Where to look / how to identify it:
  - Run tests in a production-like environment with realistic runtime integrations.
- Exploitation / test pattern:
  - Compare runtime behavior against security expectations and collect memory/network/error evidence.
- Tools + exact CLI syntax (if mentioned):
  - Book examples include IBM AppScan, Veracode, Iroh.
- Common false-positive / WAF / edge-case notes:
  - Dynamic analysis is slower, more expensive, and environment dependent.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Automate repeatable dynamic tests in CI/staging and keep test environments representative.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
