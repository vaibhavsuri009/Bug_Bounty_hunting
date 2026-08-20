# Software Version Disclosure

- **What it is:** Server responses reveal exact framework or software versions that can aid vulnerability research.
- **Where to look:** HTTP response headers, error pages, banners, and generated HTML.
- **Test / exploitation:**
  - Proxy normal responses and inspect headers such as X-Powered-By.
  - Record exact software/framework version strings.
  - Correlate disclosures with other recon evidence before acting on them.
  - Use version data to prioritize review of relevant known vulnerabilities within scope.
  - Treat the leak by itself according to program severity rules.
- **Tools / syntax:**
```text
X-Powered-By: PHP/5.2.17
```
- **False positives / edge cases:**
  - A version string may be generic, hidden, or deliberately altered; do not assume it is authoritative without corroboration.
- **Remediation:** Remove unnecessary version banners and return generic errors.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
