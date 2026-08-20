# Disable XML External Entities

- What it is: The primary XXE defense is disabling DTD/external entity resolution in every XML parser used by the application.
- Where to look / how to identify it:
  - Inventory all XML/SVG/office/XML-derived parsers and verify their secure configuration.
- Exploitation / test pattern:
  - Use parser-specific secure flags and test with a harmless external-entity sample in staging.
- Tools + exact CLI syntax (if mentioned):
  - Book Java example: `factory.setFeature(...disallow-doctype-decl, true)`.
- Common false-positive / WAF / edge-case notes:
  - Secure defaults differ by parser/language/version; never assume XXE is disabled.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Explicitly disable external entities and DTD processing wherever not required.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 30
