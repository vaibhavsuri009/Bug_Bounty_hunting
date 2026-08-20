# REST Resource + HTTP Verb Inference

- What it is: REST endpoints commonly use hierarchical resources with HTTP verbs that describe intended actions.
- Where to look / how to identify it:
  - From a known resource path, identify whether GET, POST, PUT, and DELETE map to read/create/update/delete behavior.
- Exploitation / test pattern:
  - Use documented or observed methods to understand the resource model before testing authorization.
- Tools + exact CLI syntax (if mentioned):
  - Example structure from the book: `/moderators/joe/logs/...`.
- Common false-positive / WAF / edge-case notes:
  - Do not assume every REST-like API follows REST conventions exactly.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Explicitly allow only required HTTP methods and enforce authorization consistently across them.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
