# Serialization Type Allowlist

- What it is: Allowlisting accepted serialized object types and characters limits gadget/object-injection opportunities.
- Where to look / how to identify it:
  - Review endpoints that deserialize client-controlled complex objects.
- Exploitation / test pattern:
  - Accept only expected primitive/object shapes and reject unsupported class/type metadata.
- Tools + exact CLI syntax (if mentioned):
  - Schema validation.
- Common false-positive / WAF / edge-case notes:
  - Character filtering alone is not sufficient for unsafe native object deserialization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer simple data formats plus strict schemas and never deserialize arbitrary classes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 33
