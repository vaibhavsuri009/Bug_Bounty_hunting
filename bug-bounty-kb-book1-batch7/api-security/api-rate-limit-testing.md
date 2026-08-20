# API: Rate-Limit Testing

- **What it is:** Determine whether critical API actions can be called repeatedly without effective throttling.
- **High-value endpoints:** Authentication, unauthenticated object access, and endpoints returning sensitive data.
- **Method from source:** With explicit permission, send a controlled burst (book suggests roughly 100–200 requests) using Burp Intruder or curl and observe throttling.
- **Repeat:** Test different authentication/privilege states because limits may differ.
- **Exploitability:** Lack of rate limiting matters when it enables brute force, ID harvesting, or sensitive-data enumeration.
- **Safety:** The book explicitly warns this can cause DoS; obtain written permission and throttle to program policy.
- **Remediation:** Enforce per-user/token/IP/action limits and abuse detection on sensitive routes.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
