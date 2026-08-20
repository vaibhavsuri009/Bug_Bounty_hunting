# API Recon: Public and Exposed Swagger Documentation

- **What it is:** Use API documentation to build a comprehensive endpoint/parameter map.
- **Where to look:** Official developer docs and accidentally exposed internal Swagger documentation.
- **Search pattern from source:** `company_name inurl:swagger`.
- **Method:** Record endpoints, methods, parameters, sample bodies/responses, auth requirements, and version information.
- **Key warning:** Public docs may omit private/internal endpoints; do not treat them as complete.
- **False positives:** Exposed documentation is not necessarily a vulnerability unless it reveals sensitive or unauthorized functionality.
- **Remediation:** Protect internal API docs and keep production documentation scoped to intended consumers.

```text
company_name inurl:swagger
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
