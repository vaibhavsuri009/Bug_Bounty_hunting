# JSON Boundary for Third-Party Integration

- What it is: A narrow JSON HTTP interface can reduce script/runtime coupling between first-party code and a risky dependency.
- Where to look / how to identify it:
  - Use a dedicated service to consume structured inputs and return structured results.
- Exploitation / test pattern:
  - Reject executable or unexpected formats at the boundary.
- Tools + exact CLI syntax (if mentioned):
  - HTTP JSON service/API.
- Common false-positive / WAF / edge-case notes:
  - JSON is not inherently safe if downstream code evaluates strings or trusts fields blindly.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use schema validation, strict fields, and no code evaluation at service boundaries.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
