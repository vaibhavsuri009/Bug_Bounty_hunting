# Code Review: Trace Security-Critical Functions

- **What it is:** Deep review focused on functions where a bug has immediate security impact.
- **Where to look:** Authentication, password reset/change, state-changing actions, sensitive reads, and authorization checks.
- **Method:** Read the critical function, identify inputs, validation, database calls, authorization, and downstream side effects.
- **Example from source:** Concatenating username/password directly into a SQL query creates SQL injection.
- **Priority:** Also review how critical components call and trust other components.
- **False positives:** A suspicious line may be protected by validation performed earlier; trace the full call chain.
- **Remediation:** Centralize security checks and use safe data-access / authorization primitives.

```sql
SELECT * FROM users WHERE username = 'USER_INPUT' AND password = 'USER_INPUT';
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
