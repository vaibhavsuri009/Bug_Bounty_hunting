# Certificate SAN Host Enumeration

- What it is: Extract hostnames from TLS certificate Subject Alternative Name (SAN) fields.
- Search a target domain in certificate-transparency databases.
- Sources mentioned: crt.sh, Censys, Cert Spotter.
- Review SAN entries for wildcard and explicit DNS names.
- Add unique hostnames to the recon target list after checking scope.
- crt.sh JSON output pattern:
```text
https://crt.sh/?q=example.com&output=json
```
- Parse JSON results to automate hostname extraction.
- Certificates can reveal sibling domains and subdomains that are not linked from the main site.
- Combine certificate-derived names with subdomain enumeration tools for broader coverage.
- False-positive trap: certificates may contain historical, third-party, or out-of-scope hostnames.
- Remediation: N/A — certificate transparency is public by design; avoid placing unnecessary names on shared certificates.

## Source: Bug Bounty Bootcamp, Ch. 5
