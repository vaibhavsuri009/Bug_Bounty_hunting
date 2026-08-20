# State-Changing GET CSRF

- What it is: CSRF can occur when a state-changing action is exposed through a GET request and the browser automatically includes the user's authenticated state.
- Where to look / how to identify it:
  - Identify GET endpoints that modify account state, settings, transfers, or other server-side data.
- Exploitation / test pattern:
  - Use only a controlled test account and confirm whether a normal cross-site GET can trigger the action without an anti-CSRF control.
- Tools + exact CLI syntax (if mentioned):
  - Browser/DevTools; no specialized tooling required.
- Common false-positive / WAF / edge-case notes:
  - GET requests that only read data are not CSRF targets; the endpoint must change state.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use non-GET methods for state changes, require CSRF protection, and apply SameSite cookies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
