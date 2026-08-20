# Mutation-Based XSS Signal

- What it is: Mutation XSS uses browser parsing/normalization to transform sanitizer-approved markup into executable markup after insertion.
- Where to look / how to identify it:
  - Prioritize applications that sanitize HTML and later reparse it with `innerHTML`, templates, SVG, MathML, or browser-generated DOM.
- Exploitation / test pattern:
  - Compare sanitizer output with final browser DOM and look for structural mutations.
- Tools + exact CLI syntax (if mentioned):
  - DOM inspector and sanitizer test environment.
- Common false-positive / WAF / edge-case notes:
  - mXSS is highly parser/version dependent; reproduce in the affected browser environment.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use maintained sanitizers, keep them updated, and avoid unsafe reparsing after sanitization.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
