# Fuzzing: Triage Response Anomalies

- **What it is:** Identify likely vulnerabilities by finding responses that differ from the baseline/payload majority.
- **Path fuzzing:** 2xx can indicate a valid path; 404 commonly indicates missing content.
- **SQLi indicators:** Response length changes, unusual status codes, or consistent payload-triggered timing delays.
- **General method:** Group normal responses, isolate outliers, replay manually, and confirm the behavior is payload-dependent.
- **Why it matters:** Fuzzers surface suspicious spots; manual validation determines exploitability and impact.
- **False positives:** Rate limiting, caching, load balancers, and transient failures can create anomalies.
- **Remediation:** Fix the underlying bug, then add regression tests for the triggering input.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.
- **Validation:** Confirm behavior with a controlled test before reporting.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
