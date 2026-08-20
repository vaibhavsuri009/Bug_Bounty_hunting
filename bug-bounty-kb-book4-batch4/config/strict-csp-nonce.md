# Nonce-Based Strict CSP

- What it is: Nonce-based strict CSP allows authorized inline scripts while blocking injected scripts that lack the per-response nonce.
- Where to look / how to identify it:
  - Inspect `script-src` for a nonce plus `strict-dynamic` and verify nonces change between page loads.
- Exploitation / test pattern:
  - Use a harmless test page to confirm scripts without the nonce are blocked.
- Tools + exact CLI syntax (if mentioned):
  - Browser console + response headers.
- Common false-positive / WAF / edge-case notes:
  - Static or reused nonces defeat the security model.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Generate high-entropy unique nonces per response and attach them only to trusted scripts.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
