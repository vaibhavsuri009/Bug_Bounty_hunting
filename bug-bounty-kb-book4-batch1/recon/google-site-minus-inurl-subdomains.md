# Google `site:` + `-inurl:` Subdomain Discovery

- What it is: Search-engine operators can reduce common-domain noise and surface indexed subdomains.
- Where to look / how to identify it:
  - Start with `site:target.tld`, then exclude known hosts or URL patterns with `-inurl:`.
- Exploitation / test pattern:
  - Iteratively exclude uninteresting known results and record newly discovered in-scope hosts.
- Tools + exact CLI syntax (if mentioned):
  - Example: `site:mega-bank.com -inurl:www -inurl:mobile`
- Common false-positive / WAF / edge-case notes:
  - `-inurl:` filters the entire URL, so it can accidentally hide useful pages containing the excluded text elsewhere.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Remove sensitive hosts from public indexing where appropriate and enforce security independent of obscurity.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
