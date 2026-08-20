# SQL Database Fingerprinting

- **What it is:** A confirmed SQL injection can reveal the database engine/version so later payloads use correct syntax.
- **Where to look:** UNION, error-based, Boolean, or time-based SQL injection points.
- Query a database-specific version function through the injection.

```text
MySQL / SQL Server: @@version
PostgreSQL: version()
Oracle: v$version
```

- For UNION attacks, match the number of output columns with dummy values as needed.
- Compare which version expression executes successfully.
- Use the identified engine to choose correct metadata tables and functions.
- **False positives / edge cases:** Middleware may rewrite errors; use more than one engine-specific behavior before concluding the backend type.
- **Remediation:** Parameterized queries prevent attackers from running database fingerprinting expressions.

## Source: Bug Bounty Bootcamp, Ch. 11
