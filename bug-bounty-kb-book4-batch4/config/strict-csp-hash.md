# Hash-Based Strict CSP

- What it is: Hash-based strict CSP authorizes specific inline script content by listing cryptographic hashes in `script-src`.
- Where to look / how to identify it:
  - Review hashes for trusted inline scripts and whether unauthorized inline content is blocked.
- Exploitation / test pattern:
  - Use a harmless modified script in a test build to confirm the hash mismatch blocks execution.
- Tools + exact CLI syntax (if mentioned):
  - Browser console + CSP headers.
- Common false-positive / WAF / edge-case notes:
  - Any script content change requires updating the hash.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use SHA-256+ hashes and automate CSP hash generation in the build pipeline.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
