# Historical Archive URL Discovery

- What it is: Historical web snapshots may contain links to old subdomains, file servers, downloads, and endpoints no longer visible in the live application.
- Where to look / how to identify it:
  - Inspect widely spaced archive dates, view saved page source, and search for URL schemes and hostnames.
- Exploitation / test pattern:
  - Compare historical hosts against the current asset inventory before any interaction.
- Tools + exact CLI syntax (if mentioned):
  - Search source for `http://`, `https://`, `file://`, `ftp://`, `ftps://`.
- Common false-positive / WAF / edge-case notes:
  - Archived links can be dead, transferred, or out of scope; verify ownership first.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Retire DNS/routes cleanly and remove sensitive references when decommissioning services.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
