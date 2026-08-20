# Second-Order SQL Injection

- **What it is:** Malicious input is stored safely at first, then later retrieved and inserted unsafely into another SQL query.
- **Where to look:** Signup/profile fields, saved settings, imported data, logs, and any stored value reused in backend queries.
- Store a harmless SQL test string in a controlled field.
- Trigger a later feature that reads that stored value and performs a database operation.
- Observe whether the second operation changes behavior or produces SQL errors.
- The injection point and execution point may be different endpoints.
- There may be a significant time delay between storage and execution.
- For delayed cases, the book demonstrates writing controlled query output to a web-accessible file to confirm execution.
- Revisit workflows that consume the stored value in scheduled jobs, exports, reports, or authenticated views.
- **False positives / edge cases:** Do not assume stored special characters are exploitable until a later query actually interprets them as SQL.
- **Remediation:** Parameterize every database query, including those built from previously stored application data.

## Source: Bug Bounty Bootcamp, Ch. 11
