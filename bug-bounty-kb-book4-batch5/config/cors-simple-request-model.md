# CORS Simple Request Model

- What it is: Simple CORS requests use a limited set of methods, headers, and content types and rely on Origin/Access-Control-Allow-Origin matching.
- Where to look / how to identify it:
  - Review cross-origin GET/HEAD/POST requests and whether they meet the safelisted header/content-type conditions.
- Exploitation / test pattern:
  - Use a controlled alternate origin and confirm the browser blocks response access when the server does not authorize that origin.
- Tools + exact CLI syntax (if mentioned):
  - Browser DevTools Network/Console.
- Common false-positive / WAF / edge-case notes:
  - A cross-origin request may still reach the server even when the browser blocks script access to the response.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Allow only required origins and keep state-changing endpoints protected independently of CORS.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
