# Code Review: Weak Redirect Validation

- **What it is:** Open redirect caused by sending user-controlled locations to the `Location` header with missing or weak validation.
- **Where to look:** `next`, `redirect`, `return`, or similar parameters passed to redirect/location APIs.
- **Basic flaw:** Directly assigning `$_GET['next']` to a `Location` header permits arbitrary destinations.
- **Weak-regex flaw:** Checking only whether the URL contains `example.com` can accept attacker-controlled hosts.
- **Bypass patterns from source:** `attacker.com/example.com` or `example.com.attacker.com` against substring validation.
- **False positives:** Confirm browser navigation reaches an attacker-controlled origin.
- **Remediation:** Parse the URL and enforce an exact allowlist of scheme + host + permitted path.

```http
GET /login?next=https://example.com.attacker.com HTTP/1.1
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
