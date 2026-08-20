# Social Media Subdomain OSINT

- What it is: Public social posts can expose campaign, hiring, support, product, and marketing subdomains not easily found through dictionaries.
- Where to look / how to identify it:
  - Search authorized target references and extract links pointing to the target's domain.
- Exploitation / test pattern:
  - Prioritize lower-volume or historical posts when search engines have not indexed the content.
- Tools + exact CLI syntax (if mentioned):
  - Use official social/search APIs where terms and authorization permit.
- Common false-positive / WAF / edge-case notes:
  - Social links may point to third-party services or expired domains; verify scope.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Track externally advertised assets and decommission campaigns cleanly.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
