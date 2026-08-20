# CSP Delivery via Header or Meta

- What it is: Content Security Policy can be delivered as an HTTP response header or HTML meta policy to restrict browser resource execution.
- Where to look / how to identify it:
  - Inspect every HTML response for `Content-Security-Policy` or a CSP meta element.
- Exploitation / test pattern:
  - Validate that the effective policy is consistent across sensitive pages.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Security/Network headers.
- Common false-positive / WAF / edge-case notes:
  - Deprecated `X-Content-Security-Policy` and `X-WebKit-CSP` should not be treated as modern CSP.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer a consistent CSP response header generated centrally.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
