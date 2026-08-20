# Cookie Domain Attribute Risk

- What it is: Adding a Domain attribute broadens cookie delivery to subdomains and can increase account-takeover impact if a subdomain is compromised.
- Where to look / how to identify it:
  - Inspect whether session cookies use `Domain=parent.tld` instead of host-only scope.
- Exploitation / test pattern:
  - Map which subdomains receive the cookie using controlled browser requests.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Application → Cookies.
- Common false-positive / WAF / edge-case notes:
  - Cross-subdomain SSO may legitimately require Domain-scoped cookies.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer host-only cookies; if sharing is required, secure every receiving subdomain.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 22
