# Tabnabbing Defense with COOP

- What it is: COOP `same-origin` isolates opener relationships and prevents cross-origin pages from controlling the opener browsing context.
- Where to look / how to identify it:
  - Apply to pages that open untrusted or user-generated external links.
- Exploitation / test pattern:
  - Verify controlled external pages cannot access useful opener references.
- Tools + exact CLI syntax (if mentioned):
  - `Cross-Origin-Opener-Policy: same-origin`
- Common false-positive / WAF / edge-case notes:
  - Complex multi-domain apps may need relaxed COOP behavior.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use strict COOP by default and add exceptions only for required workflows.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
