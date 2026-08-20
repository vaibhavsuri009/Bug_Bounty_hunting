# JavaScript Global Variable Exposure

- What it is: JavaScript variables created without `var`, `let`, or `const` are placed in global scope and can also become properties of `window`.
- Where to look / how to identify it:
  - Review client-side source for unintended global variables, especially values containing state, IDs, tokens, configuration, or privileged flags.
- Exploitation / test pattern:
  - Inspect `window` and source code in DevTools on an authorized application.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Console: inspect `window` or specific suspected global names.
- Common false-positive / WAF / edge-case notes:
  - Global visibility is not automatically exploitable; determine whether the value is sensitive or security-relevant.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use `let`/`const`, modular scopes, and avoid storing sensitive authorization decisions client-side.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
