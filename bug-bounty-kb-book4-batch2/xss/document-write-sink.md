# `document.write()` XSS Sink

- What it is: `document.write()` parses supplied text into the active DOM and can execute markup/script when fed untrusted data.
- Where to look / how to identify it:
  - Search JavaScript for `document.write`/`writeln` and trace argument origin.
- Exploitation / test pattern:
  - Confirm only with a benign source-to-sink test in an authorized browser.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Sources search for `document.write`.
- Common false-positive / WAF / edge-case notes:
  - Static strings are safe; risk requires attacker-controlled data.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Avoid `document.write()` with untrusted input and use safe DOM construction.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
