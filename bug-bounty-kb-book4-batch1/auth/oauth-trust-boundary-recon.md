# OAuth Trust-Boundary Recon

- What it is: OAuth lets one service provide identity or authorization tokens to another, introducing a trust relationship across applications.
- Where to look / how to identify it:
  - Map identity provider, relying application, redirect/callback locations, tokens, scopes, and account-linking behavior.
- Exploitation / test pattern:
  - Record which applications share identity and what a compromise of one party could affect.
- Tools + exact CLI syntax (if mentioned):
  - Browser Network/XHR tracing during login.
- Common false-positive / WAF / edge-case notes:
  - OAuth use itself is not a weakness; implementation and trust configuration determine risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Strictly validate redirects, scopes, state/nonce, issuer/audience, and token lifecycle.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
