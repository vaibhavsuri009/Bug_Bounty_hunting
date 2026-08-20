# `noopener noreferrer` for Dynamic Links

- What it is: `noopener` blocks access to `window.opener`; `noreferrer` also suppresses referrer leakage.
- Where to look / how to identify it:
  - Add both attributes to untrusted external links, especially dynamically generated ones.
- Exploitation / test pattern:
  - Verify the target page cannot navigate the opener and receives no unnecessary referrer.
- Tools + exact CLI syntax (if mentioned):
  - `rel='noopener noreferrer'`
- Common false-positive / WAF / edge-case notes:
  - Modern browsers may imply noopener in some cases, but explicit protection is clearer.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Set both attributes on untrusted new-tab links.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
