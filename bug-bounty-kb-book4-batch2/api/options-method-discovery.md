# OPTIONS Method Discovery

- What it is: HTTP OPTIONS can disclose which request methods an API declares as supported.
- Where to look / how to identify it:
  - Try OPTIONS first against a known authorized endpoint when the engagement allows it.
- Exploitation / test pattern:
  - Record the `Allow` response and compare it with methods observed in the application.
- Tools + exact CLI syntax (if mentioned):
  - `curl -i -X OPTIONS https://api.target.tld/resource`
- Common false-positive / WAF / edge-case notes:
  - Enterprise APIs may disable OPTIONS even when other methods exist.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Expose only required methods and return minimal method metadata.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
