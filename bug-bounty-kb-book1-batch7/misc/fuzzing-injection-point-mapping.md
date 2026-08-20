# Fuzzing: Map Data Injection Points

- **What it is:** Identify every location a web fuzzer can mutate before selecting payloads.
- **Where to look:** URL paths, query parameters, body parameters, headers, cookies, and other user-controlled fields.
- **Method:** Mark candidate values with a placeholder such as `FUZZ` and classify each by likely vulnerability.
- **Examples from source:** Numeric IDs → IDOR; search input → reflected XSS.
- **Goal:** Build a target-specific matrix of injection point × vulnerability class.
- **False positives:** Not every client-controlled field reaches sensitive logic; prioritize fields that affect server behavior.
- **Remediation:** Validate all untrusted inputs at server-side trust boundaries.

```http
GET /email_inbox?user_id=FUZZ
GET /search?q=FUZZ
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
