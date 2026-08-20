# CSRF Content-Type Validation Gap

- What it is: Some endpoints apply CSRF validation only to one expected content type and process alternate formats through a weaker code path.
- Where to look / how to identify it:
  - Compare the same harmless state-changing request across accepted content types on a controlled account.
- Exploitation / test pattern:
  - Check whether validation disappears when the request format changes but the business action still succeeds.
- Tools + exact CLI syntax (if mentioned):
  - DevTools/Burp/Postman; edit only `Content-Type` and matching body format.
- Common false-positive / WAF / edge-case notes:
  - Most alternate types will simply fail parsing; acceptance alone is not a vulnerability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply CSRF validation after request parsing and independent of content type.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
