# Dangerous DOM Sink Reduction

- What it is: APIs that convert strings into executable DOM or script are high-risk XSS sinks.
- Where to look / how to identify it:
  - Search for `innerHTML`, `outerHTML`, Blob, SVG, `document.write`, DOMParser, and implementation APIs.
- Exploitation / test pattern:
  - Replace sinks with explicit node creation or safe text insertion where feasible.
- Tools + exact CLI syntax (if mentioned):
  - `document.createElement()` + `appendChild()`.
- Common false-positive / WAF / edge-case notes:
  - A sink can be safe with trusted constant input; data flow matters.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Eliminate unnecessary sinks and wrap unavoidable ones with reviewed sanitization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
