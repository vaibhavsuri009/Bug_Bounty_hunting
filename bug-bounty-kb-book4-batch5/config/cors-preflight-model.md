# CORS Preflight Model

- What it is: Non-simple cross-origin requests trigger an OPTIONS preflight containing origin, requested method, and requested headers.
- Where to look / how to identify it:
  - Inspect OPTIONS traffic before PUT/PATCH/DELETE or requests with non-safelisted headers.
- Exploitation / test pattern:
  - Verify the server allows only explicitly required origins, methods, and headers.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network or curl OPTIONS against a test endpoint.
- Common false-positive / WAF / edge-case notes:
  - Preflight success does not replace authentication or authorization.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Implement least-privilege CORS middleware and reject unknown origins/methods/headers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
