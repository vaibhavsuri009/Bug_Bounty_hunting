# Hyperlink Canonicalization

- What it is: User-controlled navigation values can become script or redirect vectors when concatenated directly into location APIs.
- Where to look / how to identify it:
  - Review `window.location`, anchor href generation, redirect helpers, and user-submitted links.
- Exploitation / test pattern:
  - Parse with a browser/URL API and allow only intended schemes/origins before navigation.
- Tools + exact CLI syntax (if mentioned):
  - URL/anchor parsing APIs; `encodeURIComponent` for components.
- Common false-positive / WAF / edge-case notes:
  - Encoding an entire URL can break the URI structure; encode individual components instead.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize and allowlist schemes/origins before using user-controlled links.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
