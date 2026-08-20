# Session-Bound CSRF Token

- What it is: A cryptographically strong CSRF token tied to a specific user/session prevents another origin from forging state-changing requests.
- Where to look / how to identify it:
  - Verify every form/AJAX state-changing request carries a live user-bound token.
- Exploitation / test pattern:
  - Reject expired, altered, missing, or cross-user tokens.
- Tools + exact CLI syntax (if mentioned):
  - Framework anti-CSRF middleware.
- Common false-positive / WAF / edge-case notes:
  - Global token pools or predictable values weaken the defense.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Generate high-entropy per-session/per-request tokens and validate server-side.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 29
