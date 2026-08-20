# `innerHTML` XSS Sink

- What it is: `element.innerHTML` interprets attacker-controlled strings as DOM markup and is a common XSS sink.
- Where to look / how to identify it:
  - Search client code for assignments to `innerHTML` and trace the assigned value back to user-controlled sources.
- Exploitation / test pattern:
  - Use benign markup first to prove the source-to-sink path before any harmless script test.
- Tools + exact CLI syntax (if mentioned):
  - Source review or DevTools Sources search for `innerHTML`.
- Common false-positive / WAF / edge-case notes:
  - Sanitized values may be safe; verify the sanitizer and context.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer `innerText`/`textContent`; sanitize required HTML with a well-tested library.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
