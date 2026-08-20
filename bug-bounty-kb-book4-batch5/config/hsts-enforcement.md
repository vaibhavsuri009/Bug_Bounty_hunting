# HSTS Enforcement

- What it is: HSTS tells browsers to use HTTPS for a host and optionally all subdomains, preventing future cleartext HTTP use.
- Where to look / how to identify it:
  - Inspect for `Strict-Transport-Security` on HTTPS responses and note max-age, includeSubDomains, and preload.
- Exploitation / test pattern:
  - Verify HTTP navigation upgrades safely in a test browser without exposing credentials.
- Tools + exact CLI syntax (if mentioned):
  - `Strict-Transport-Security: max-age=<seconds>; includeSubDomains; preload`
- Common false-positive / WAF / edge-case notes:
  - HSTS is ignored when delivered over insecure HTTP and can cause outages if subdomains are not HTTPS-ready.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Deploy HSTS on HTTPS, use a safe rollout, then consider includeSubDomains/preload.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
