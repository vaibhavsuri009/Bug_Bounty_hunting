# HTML Entity Encoding

- What it is: HTML entity encoding prevents key markup characters from being interpreted as DOM when data is inserted into ordinary HTML text contexts.
- Where to look / how to identify it:
  - Encode ampersand, angle brackets, quotes, and apostrophes before HTML rendering.
- Exploitation / test pattern:
  - Validate output in the exact rendering context used by the application.
- Tools + exact CLI syntax (if mentioned):
  - Template/output-encoding library.
- Common false-positive / WAF / edge-case notes:
  - Entity encoding does not protect JavaScript, CSS, URL, or script-tag contexts.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use context-specific output encoding rather than a single universal encoder.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
