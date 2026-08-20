# Reflected Query-Parameter XSS

- What it is: Reflected XSS occurs when request input is immediately inserted into the returned page without safe encoding.
- Where to look / how to identify it:
  - Look for search terms, errors, names, and query parameters echoed into HTML or script contexts.
- Exploitation / test pattern:
  - Insert a unique marker, locate its output context, then use a harmless context-appropriate proof.
- Tools + exact CLI syntax (if mentioned):
  - Browser URL bar + View Source/DevTools.
- Common false-positive / WAF / edge-case notes:
  - Reflection alone is not XSS; browser script execution must be possible.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Perform context-aware output encoding and avoid unsafe DOM/string concatenation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
