# BOLA via Nested JSON Object

- What it is: Nested JSON can bypass authorization or validation applied only to an outer scalar field.
- Where to look / how to identify it:
  - Where an endpoint expects a scalar object ID, test the equivalent nested object shape using IDs from controlled accounts, e.g. `{"Account":{"Account":3333}}`.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Parser coercion/errors alone are not authorization bypass.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce schema and authorization after parsing the final canonical object.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
