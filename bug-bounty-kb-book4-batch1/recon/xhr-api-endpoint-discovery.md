# XHR/Fetch API Endpoint Discovery

- What it is: XHR/fetch filtering removes images/fonts and highlights API-like browser requests such as GET, POST, PUT, and DELETE.
- Where to look / how to identify it:
  - Use the Network panel's Fetch/XHR filter while navigating application workflows.
- Exploitation / test pattern:
  - Inspect request URL, headers, body, Preview, Response, and method; add endpoints to the recon map.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network → Fetch/XHR.
- Common false-positive / WAF / edge-case notes:
  - Not every XHR request is an API endpoint worth testing; identify business functionality first.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Document APIs and expose only required routes/methods.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
