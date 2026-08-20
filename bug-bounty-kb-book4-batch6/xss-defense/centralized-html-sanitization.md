# Centralized HTML Sanitization

- What it is: When user content must contain allowed HTML, sanitization should occur through one reviewed application-wide helper.
- Where to look / how to identify it:
  - Identify every path that converts user-controlled strings into DOM.
- Exploitation / test pattern:
  - Route those paths through a maintained sanitizer rather than per-feature regex filters.
- Tools + exact CLI syntax (if mentioned):
  - Trusted sanitizer library such as DOMPurify-style tooling.
- Common false-positive / WAF / edge-case notes:
  - Homegrown tag blocklists miss URL schemes, parser mutations, SVG, and other execution paths.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use one maintained sanitizer and regression-test dangerous contexts.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
