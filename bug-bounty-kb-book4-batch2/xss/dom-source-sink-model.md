# DOM XSS Source/Sink Model

- What it is: DOM XSS requires an attacker-controlled source and a script-capable DOM sink; no server interaction is necessary.
- Where to look / how to identify it:
  - Trace values from `location`, storage, referrer, window state, or other client sources into DOM-writing/executing APIs.
- Exploitation / test pattern:
  - Prove the exact source-to-sink flow in the browser using a harmless payload.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Sources/Debugger/Console.
- Common false-positive / WAF / edge-case notes:
  - Client-side source use without a dangerous sink is not exploitable.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use safe DOM APIs and sanitize/validate before dangerous sinks.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
