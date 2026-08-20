# Affiliated Domain Discovery via Browser Network

- What it is: Background requests made by the visible application can reveal additional API, media, authentication, logging, and service subdomains.
- Where to look / how to identify it:
  - Browse normal functionality with DevTools Network open and inspect each request's destination URL.
- Exploitation / test pattern:
  - Record new in-scope domains/hosts and classify their purpose.
- Tools + exact CLI syntax (if mentioned):
  - Chrome/Firefox/Edge DevTools → Network.
- Common false-positive / WAF / edge-case notes:
  - Third-party analytics/CDNs may not belong to the target; verify ownership and scope.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain a public asset inventory and minimize unnecessary cross-domain dependencies.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
