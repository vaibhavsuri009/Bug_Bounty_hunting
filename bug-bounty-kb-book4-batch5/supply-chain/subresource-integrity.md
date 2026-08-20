# Subresource Integrity

- What it is: SRI verifies that a third-party script/style has not changed since its trusted hash was generated.
- Where to look / how to identify it:
  - Inspect external script/style tags for integrity attributes and matching crossorigin configuration.
- Exploitation / test pattern:
  - In a test environment, change the hosted file and verify the browser refuses the mismatched resource.
- Tools + exact CLI syntax (if mentioned):
  - `integrity='sha384-...' crossorigin='anonymous'`
- Common false-positive / WAF / edge-case notes:
  - SRI is hard to use for frequently changing third-party assets unless versions are pinned.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Pin third-party resources and use SRI for static externally hosted dependencies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
