# POST Form CSRF

- What it is: HTML forms can submit cross-origin POST requests using browser-authenticated state when the server lacks CSRF defenses.
- Where to look / how to identify it:
  - Look for sensitive POST endpoints that accept standard form encodings and rely only on session cookies.
- Exploitation / test pattern:
  - Build a controlled form using test-account values and verify whether the server accepts the cross-site request.
- Tools + exact CLI syntax (if mentioned):
  - Standard HTML `<form method='POST'>` is sufficient for validation.
- Common false-positive / WAF / edge-case notes:
  - JSON-only endpoints and custom-header requirements may prevent basic form delivery.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Require unpredictable per-session/per-request CSRF tokens plus SameSite cookies and origin validation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
