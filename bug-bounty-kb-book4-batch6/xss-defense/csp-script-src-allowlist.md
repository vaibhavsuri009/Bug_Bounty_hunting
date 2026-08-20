# CSP Script Source Allowlist

- What it is: `script-src` limits which origins may supply executable JavaScript and can reduce the impact of stored/reflected script injection.
- Where to look / how to identify it:
  - Review the exact script origins required by each application.
- Exploitation / test pattern:
  - Start from self and narrowly required hosts; avoid organization-wide wildcards.
- Tools + exact CLI syntax (if mentioned):
  - `Content-Security-Policy: script-src 'self' https://api.example.com`
- Common false-positive / WAF / edge-case notes:
  - An allowed origin that later hosts user-controlled scripts can become an XSS path.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep script origin lists narrow and review new subdomains/integrations.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 28
