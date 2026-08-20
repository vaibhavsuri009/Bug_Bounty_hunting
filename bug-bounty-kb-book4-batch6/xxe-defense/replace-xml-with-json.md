# Replace XML with Simpler Data Formats

- What it is: Applications using XML only for lightweight structured API data may eliminate XXE risk by moving to JSON or another simpler format.
- Where to look / how to identify it:
  - Determine whether XML-specific features such as mixed content, rendering, metadata, or schema validation are actually required.
- Exploitation / test pattern:
  - Re-architect compatible API payloads to JSON in a controlled migration.
- Tools + exact CLI syntax (if mentioned):
  - API schema/versioning tools.
- Common false-positive / WAF / edge-case notes:
  - JSON has its own risks and is not a universal replacement for XML-derived document formats.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use the simplest format that meets business requirements and validate its schema.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 30
