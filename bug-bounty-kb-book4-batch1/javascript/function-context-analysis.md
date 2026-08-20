# JavaScript Function Context Analysis

- What it is: JavaScript function behavior can change depending on `this` context, and context can be moved with `bind`, `call`, and `apply`.
- Where to look / how to identify it:
  - Review client logic that moves context between security-relevant objects or functions.
- Exploitation / test pattern:
  - Trace where attacker-influenced objects may become a function's context and whether privileged properties are read from `this`.
- Tools + exact CLI syntax (if mentioned):
  - Manual code review and DevTools debugger.
- Common false-positive / WAF / edge-case notes:
  - Context complexity is only a risk signal; verify that it changes a security decision or sink.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reduce dynamic context use around security logic and add tests for authorization-sensitive code.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
