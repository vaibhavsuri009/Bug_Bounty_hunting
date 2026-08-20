# Static XSS Rule Patterns

- What it is: Simple source patterns can surface likely XSS sources and sinks for manual review.
- Where to look / how to identify it:
  - Search for `innerHTML`, URL-derived variables, DOM sinks such as string-executing timer APIs, and unsafe rendering helpers.
- Exploitation / test pattern:
  - Trace data flow rather than reporting keyword matches directly.
- Tools + exact CLI syntax (if mentioned):
  - SAST/source search.
- Common false-positive / WAF / edge-case notes:
  - Keyword presence alone is not a vulnerability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use safe DOM APIs and centralized sanitization/output encoding.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
