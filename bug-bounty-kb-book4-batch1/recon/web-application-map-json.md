# JSON-Style Recon Mapping

- What it is: A hierarchical recon map preserves relationships among endpoints, methods, request shapes, features, integrations, and roles.
- Where to look / how to identify it:
  - For each endpoint, record URL, HTTP method, required fields, types, limits, optional fields, and related business functionality.
- Exploitation / test pattern:
  - Use a consistent nested structure so related endpoints and features can be searched and revisited later.
- Tools + exact CLI syntax (if mentioned):
  - Example keys: `api_endpoints`, `features`, `integrations`, `shape`.
- Common false-positive / WAF / edge-case notes:
  - Do not store live secrets in plaintext notes; redact credentials and tokens.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain current internal API documentation and asset ownership records.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 2
