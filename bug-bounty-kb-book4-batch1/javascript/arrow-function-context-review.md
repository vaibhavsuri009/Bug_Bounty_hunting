# Arrow Function Context Review

- What it is: Arrow functions inherit context from their parent instead of creating their own `this` binding.
- Where to look / how to identify it:
  - Compare standard functions and arrow functions in code that relies on object-specific security state.
- Exploitation / test pattern:
  - Trace whether inherited context causes the application to reference a broader or unintended object.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Sources + breakpoints.
- Common false-positive / WAF / edge-case notes:
  - Unexpected `this` behavior may be a functional bug without security impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep authorization logic server-side and use explicit data flow instead of implicit context.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
