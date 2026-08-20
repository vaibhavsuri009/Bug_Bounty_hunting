# Cross-User CSRF Token Reuse

- What it is: Legacy CSRF systems may validate whether a token is in a global pool instead of binding it to the current user/session.
- Where to look / how to identify it:
  - Generate a token with test account A and submit it with a request authenticated as test account B.
- Exploitation / test pattern:
  - Use a harmless state change to prove whether another user's token is accepted.
- Tools + exact CLI syntax (if mentioned):
  - DevTools/Burp-style request replay; curl may be used for benign controlled requests.
- Common false-positive / WAF / edge-case notes:
  - A reusable token may still be scoped to a form or session despite appearing similar.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Bind CSRF tokens to user/session and validate one-time or narrowly scoped usage.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 11
