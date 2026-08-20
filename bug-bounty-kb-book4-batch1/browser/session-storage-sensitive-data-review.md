# Session Storage Sensitive Data Review

- What it is: Session storage behaves like local storage but is scoped to the lifetime of a browser tab.
- Where to look / how to identify it:
  - Inspect session storage for sensitive tokens or data that could still be exposed to same-origin script execution.
- Exploitation / test pattern:
  - Record whether authentication or authorization relies on client-controlled values.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Application/Storage panel.
- Common false-positive / WAF / edge-case notes:
  - Shorter persistence reduces exposure but does not protect against XSS or malicious same-origin scripts.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep privileged state server-side and use hardened, short-lived credentials.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
