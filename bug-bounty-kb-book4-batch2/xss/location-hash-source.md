# `window.location.hash` as XSS Source

- What it is: URL fragments are client-side data sources accessible to JavaScript and are not normally sent to the server.
- Where to look / how to identify it:
  - Search scripts for `window.location.hash` or `document.location.hash` and see how the value is consumed.
- Exploitation / test pattern:
  - Test only when the value later reaches a script-capable DOM sink.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Sources search + local URL fragment.
- Common false-positive / WAF / edge-case notes:
  - A fragment by itself is not dangerous; the sink determines exploitability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Treat location-derived values as untrusted input.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
