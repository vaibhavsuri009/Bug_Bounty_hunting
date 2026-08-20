# Swagger/OpenAPI Documentation Discovery

- What it is: REST's structured resource model makes automatic API documentation such as Swagger/OpenAPI common.
- Where to look / how to identify it:
  - Look for documentation exposed by the application, developer portals, source links, or API UI components.
- Exploitation / test pattern:
  - Use documentation to record endpoint methods, shapes, required fields, and authentication requirements.
- Tools + exact CLI syntax (if mentioned):
  - Browser search and application source/network inspection.
- Common false-positive / WAF / edge-case notes:
  - Public API documentation can be intentional; risk depends on exposed privileged details and missing controls.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Publish only necessary documentation and protect internal/admin specifications.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
