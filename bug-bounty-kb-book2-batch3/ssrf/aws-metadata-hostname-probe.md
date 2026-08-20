# SSRF AWS Metadata Hostname Probe

- What it is: SSRF can reach the AWS link-local metadata service from an EC2-hosted server.
- After internal SSRF is confirmed, a low-impact metadata check from the book is:
```text
http://169.254.169.254/latest/meta-data/hostname
```
- A returned internal hostname proves access to the metadata service.
- Stop at minimal metadata proof unless the program explicitly allows credential access.
- The book notes IAM credential paths can be far more sensitive.
- False positive: non-AWS hosts may respond differently or not at all.
- Edge case: IMDSv2 requires a token and blocks many simple SSRF techniques.
- Remediation: require IMDSv2, restrict metadata access, and block link-local destinations from fetchers.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
