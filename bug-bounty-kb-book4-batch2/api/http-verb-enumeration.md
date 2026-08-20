# HTTP Verb Enumeration

- What it is: When OPTIONS is unavailable, test expected REST verbs against a known endpoint to understand method handling.
- Where to look / how to identify it:
  - Use a known-good endpoint and compare GET, POST, PUT, PATCH, and DELETE responses only on safe test resources.
- Exploitation / test pattern:
  - Record whether a method returns a real response, timeout, or method-not-allowed behavior.
- Tools + exact CLI syntax (if mentioned):
  - Book example iterates methods with XMLHttpRequest and records status codes.
- Common false-positive / WAF / edge-case notes:
  - State-changing verbs may alter or delete data; use controlled resources and explicit permission.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use method allowlists and apply authorization consistently to every supported method.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
