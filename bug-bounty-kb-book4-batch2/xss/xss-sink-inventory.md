# XSS Sink Inventory

- What it is: Script-capable sinks include DOM and JavaScript APIs that can interpret attacker-controlled text as code or markup.
- Where to look / how to identify it:
  - Search for `eval`, script creation, `document.write`, `innerHTML`, `outerHTML`, `Function`, timers with string code, location assignment, and contextual fragment APIs.
- Exploitation / test pattern:
  - Trace each sink backward to determine whether untrusted data can reach it.
- Tools + exact CLI syntax (if mentioned):
  - Source search/static review plus DevTools.
- Common false-positive / WAF / edge-case notes:
  - Presence of a sink is not a vulnerability when input is constant or safely sanitized.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reduce dangerous sinks and enforce safe wrappers or Trusted Types.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
