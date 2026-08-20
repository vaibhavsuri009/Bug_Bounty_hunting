# CORS Weak Regex Origin Bypass

- **What it is:** An origin allowlist uses substring/prefix matching that accepts attacker-controlled domains containing the trusted hostname.
- **Where to look:** CORS endpoints that accept sibling subdomains or appear to use flexible origin validation.
- **Test / exploitation:**
  - Identify an allowed origin pattern.
  - Craft an attacker origin that contains the trusted hostname but is not actually under it.
  - Send the crafted Origin header through a proxy.
  - Check whether the server reflects it in Access-Control-Allow-Origin.
  - If reflected, verify whether authenticated sensitive data is browser-readable.
- **Tools / syntax:**
```text
Origin: https://www.example.com.attacker.com
```
- **False positives / edge cases:**
  - A well-constructed regex or exact parser-based origin check will reject this form.
- **Remediation:** Parse origins structurally and compare exact scheme/host/port against an allowlist.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
