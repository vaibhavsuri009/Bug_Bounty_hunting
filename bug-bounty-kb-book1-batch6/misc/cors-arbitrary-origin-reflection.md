# CORS Arbitrary Origin Reflection

- **What it is:** The server reflects any supplied Origin into Access-Control-Allow-Origin without validating it.
- **Where to look:** Sensitive authenticated endpoints using CORS.
- **Test / exploitation:**
  - Send a normal request and note the CORS response headers.
  - Replace Origin with a domain you control.
  - Check whether Access-Control-Allow-Origin reflects that exact origin.
  - Test from a browser context to determine whether sensitive data becomes readable cross-origin.
  - Assess only data from your test account.
- **Tools / syntax:**
```text
Origin: https://attacker.com
Access-Control-Allow-Origin: https://attacker.com
```
- **False positives / edge cases:**
  - Access-Control-Allow-Origin: * is not equivalent when credentialed requests are required.
- **Remediation:** Return ACAO only for origins in a strict allowlist.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
