# HTML Rendering as an XSS Signal

- What it is: If user-controlled text is interpreted as HTML markup rather than displayed as text, the same data flow may permit script execution.
- Where to look / how to identify it:
  - Submit benign formatting markup in an authorized test input and inspect how it is rendered.
- Exploitation / test pattern:
  - Escalate only with harmless script-execution proof after confirming the rendering context.
- Tools + exact CLI syntax (if mentioned):
  - Browser DevTools Elements/Network.
- Common false-positive / WAF / edge-case notes:
  - HTML support can be intentional; the vulnerability exists when unsafe script-capable markup is accepted.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Default to text rendering and sanitize explicitly permitted HTML.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
