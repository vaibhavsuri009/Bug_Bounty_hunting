# Protocol-Relative URL Filter Bypass Signal

- What it is: Protocol-relative URLs beginning with `//` can bypass filters that only detect explicit `http://` or `https://` strings.
- Where to look / how to identify it:
  - Review filters around externally loaded resources and permitted URL schemes.
- Exploitation / test pattern:
  - Test harmless controlled URLs using the alternate syntax only in authorized environments.
- Tools + exact CLI syntax (if mentioned):
  - Example pattern: `//example.test/resource`.
- Common false-positive / WAF / edge-case notes:
  - Modern applications may intentionally support PRURLs; impact depends on the consuming sink and CSP.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize URLs and enforce explicit HTTPS allowlists.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 10
