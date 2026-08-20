# API: Re-test Web Injection Classes Through API Inputs

- **What it is:** APIs are alternate input surfaces for the same server-side vulnerabilities found in web apps.
- **Where to look:** URL/path parameters, JSON/XML bodies, file uploads, external-URL fields, and reflected values.
- **Classes called out:** SSRF, race conditions, path traversal, file inclusion, insecure deserialization, XXE, XSS, and RCE via uploads.
- **Method:** Map the input type to the relevant payload family and send it in API-native form.
- **Examples:** External URL → SSRF test; XML → XXE test; filepath → traversal; reflected parameter → XSS.
- **False positives:** API error text can echo payloads without executing them; validate behavior/side effects.
- **Remediation:** Apply the same input validation, output encoding, and isolation controls to API endpoints as web routes.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
