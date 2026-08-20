# API Recon: Test Older API Versions

- **What it is:** Probe previous API versions for endpoints whose fixes exist only in newer versions.
- **Where to look:** Versioned routes such as `/api/v2/...`.
- **Method:** For each current endpoint, substitute older version identifiers and compare behavior/security controls.
- **Source example:** If `/api/v2/user_emails/ID` exists, test `/api/v1/user_emails/ID`.
- **Compare:** Authentication, authorization, response fields, rate limits, and input validation.
- **False positives:** Older endpoints may intentionally return compatibility errors without exposing functionality.
- **Remediation:** Decommission obsolete API versions or backport all security fixes and controls.

```http
GET /api/v2/user_emails/ID
GET /api/v1/user_emails/ID
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
