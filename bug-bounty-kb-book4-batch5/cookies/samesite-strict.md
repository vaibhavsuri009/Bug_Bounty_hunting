# SameSite Strict Cookie

- What it is: SameSite controls whether cookies accompany cross-site requests and can reduce CSRF exposure.
- Where to look / how to identify it:
  - Inspect authentication cookies for SameSite and understand whether cross-site navigation is a legitimate requirement.
- Exploitation / test pattern:
  - Use a benign controlled cross-site request to confirm cookie behavior.
- Tools + exact CLI syntax (if mentioned):
  - `Set-Cookie: ...; SameSite=Strict`
- Common false-positive / WAF / edge-case notes:
  - Strict can break legitimate SSO/payment flows; Lax may be a more compatible fallback.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use Strict where feasible, otherwise Lax plus robust CSRF tokens.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
