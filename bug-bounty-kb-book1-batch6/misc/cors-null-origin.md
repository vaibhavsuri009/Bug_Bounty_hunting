# CORS null-Origin Misconfiguration

- **What it is:** A sensitive endpoint allows the null Origin value, potentially allowing cross-origin reads from contexts that generate null origins.
- **Where to look:** Authenticated responses containing Access-Control-Allow-Origin and sensitive user data.
- **Test / exploitation:**
  - Intercept a request to the target resource.
  - Send the request with Origin: null.
  - Check whether the response returns Access-Control-Allow-Origin: null.
  - If credentials are relevant, verify whether the browser can include them in the tested flow.
  - Demonstrate access only to data belonging to your own test account.
- **Tools / syntax:**
```text
Origin: null
Access-Control-Allow-Origin: null
```
- **False positives / edge cases:**
  - A CORS header on public data has little or no security impact.
- **Remediation:** Use a strict explicit origin allowlist for sensitive resources.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 19
