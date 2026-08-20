# Strong Serializer Library Selection

- What it is: Serialization attacks are reduced by using mature, widely reviewed serialization/deserialization libraries.
- Where to look / how to identify it:
  - Inventory every serializer/deserializer and format used across service boundaries.
- Exploitation / test pattern:
  - Prefer heavily used formats and libraries with a strong security/audit history.
- Tools + exact CLI syntax (if mentioned):
  - Dependency inventory/SBOM.
- Common false-positive / WAF / edge-case notes:
  - Popular libraries can still have vulnerabilities and must be patched.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use maintained serializers, patch quickly, and avoid unsafe object-instantiation features.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 33
