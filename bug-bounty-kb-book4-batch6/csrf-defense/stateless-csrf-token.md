# Stateless CSRF Token

- What it is: Stateless APIs can carry self-contained CSRF tokens containing user identity, timestamp, and a server-verifiable nonce/signature.
- Where to look / how to identify it:
  - Inspect token contents/design for identity binding, expiration, and integrity.
- Exploitation / test pattern:
  - Validate the token without requiring server-side session storage while keeping the signing secret server-only.
- Tools + exact CLI syntax (if mentioned):
  - Cryptographic token library.
- Common false-positive / WAF / edge-case notes:
  - Encryption alone does not guarantee integrity unless the construction authenticates the token.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use authenticated cryptographic tokens with short expiry and user binding.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 29
