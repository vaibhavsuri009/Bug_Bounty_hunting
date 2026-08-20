# REST Stateless Token Model

- What it is: REST APIs are designed to be stateless; authentication and authorization context therefore travels with each request, usually as a token.
- Where to look / how to identify it:
  - Inspect requests for bearer tokens, API keys, cookies, and other authorization data sent repeatedly.
- Exploitation / test pattern:
  - Compare which endpoints require credentials and how credentials are scoped to resources.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network/XHR request headers.
- Common false-positive / WAF / edge-case notes:
  - A token being visible to its own authenticated client is normal; exposure to unauthorized parties is the issue.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use short-lived scoped tokens, secure transport, rotation, and server-side authorization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
