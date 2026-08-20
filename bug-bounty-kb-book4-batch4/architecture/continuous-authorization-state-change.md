# Continuous Authorization After Role Change

- What it is: Long-lived tokens can retain privileges after employment, role, or account state changes if authorization is only checked at token issuance.
- Where to look / how to identify it:
  - Model events such as termination, suspension, privilege reduction, password reset, and admin revocation.
- Exploitation / test pattern:
  - Verify controlled role changes immediately affect access despite an unexpired token.
- Tools + exact CLI syntax (if mentioned):
  - Auth test accounts/session management.
- Common false-positive / WAF / edge-case notes:
  - Some systems intentionally tolerate short propagation windows; document accepted maximum delay.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use short-lived tokens, revocation, session introspection, and permission checks at request time.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
