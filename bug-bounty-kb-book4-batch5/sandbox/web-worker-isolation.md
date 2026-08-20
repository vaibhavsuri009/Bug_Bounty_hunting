# Web Worker Isolation

- What it is: Web Workers run JavaScript in a separate execution context without direct DOM access, offering partial isolation.
- Where to look / how to identify it:
  - Identify third-party/background code executed in Worker contexts and messages exchanged with the main page.
- Exploitation / test pattern:
  - Review what data is passed via postMessage/MessageChannel and whether the Worker can make network requests.
- Tools + exact CLI syntax (if mentioned):
  - `new Worker('code.js')`
- Common false-positive / WAF / edge-case notes:
  - Workers are less isolated than cross-origin sandboxed iframes and can still perform network activity.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Minimize data shared with workers and validate all messages/network destinations.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
