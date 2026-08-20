# Public JavaScript Secret Hunting

- **What it is:** Public HTML/JavaScript can expose API keys, credentials, internal endpoints, and personal information.
- **Where to look:** Client-side source files loaded by normal application pages.
- **Test / exploitation:**
  - Browse as a normal user and note pages handling sensitive information.
  - View page source and enumerate referenced JavaScript files.
  - Search HTML/JS for keywords such as password and api_key.
  - Use endpoint-discovery tooling to find additional JavaScript files.
  - Validate whether any discovered credential is current before treating it as a vulnerability.
- **Tools / syntax:**
  - LinkFinder is mentioned for locating JavaScript endpoints/files.
- **False positives / edge cases:**
  - Client-side identifiers are not necessarily secrets; verify privilege and current validity.
- **Remediation:** Never embed secrets in client-delivered code; rotate any exposed credentials.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
