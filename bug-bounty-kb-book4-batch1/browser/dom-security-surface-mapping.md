# Browser DOM Security Surface Mapping

- What it is: The DOM is the browser's hierarchical interface for HTML, state, history, cookies, URLs, and other client functionality.
- Where to look / how to identify it:
  - Inspect DOM sources and JavaScript that manipulate elements, URLs, storage, or dynamic HTML.
- Exploitation / test pattern:
  - Record client-side data sources and sinks so later XSS/client-side testing can target actual data flows.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Elements, Console, Sources.
- Common false-positive / WAF / edge-case notes:
  - DOM manipulation is normal; only attacker-controlled source-to-dangerous-sink paths are security relevant.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use safe DOM APIs and enforce output encoding/sanitization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
