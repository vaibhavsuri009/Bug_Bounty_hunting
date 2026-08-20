# Code Review: Incomplete CSRF Validation

- **What it is:** CSRF protection that runs only conditionally or validates only the presence of a Referer.
- **Where to look:** State-changing endpoints and helper functions that validate CSRF tokens or Referer headers.
- **Source flaw 1:** `if csrf_token: validate_token(...)` means omitting or blanking the token skips validation.
- **Source flaw 2:** Checking only that a Referer exists does not prove it belongs to a trusted origin.
- **Test pattern:** Compare valid token, blank token, missing token, and attacker-controlled Referer behavior.
- **False positives:** Framework middleware may enforce CSRF before the reviewed function executes.
- **Remediation:** Require a valid token on every state-changing request and validate origin/Referer robustly.

```http
GET /change_password?new_password=abc&csrf_token=
GET /change_password?new_password=abc
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
