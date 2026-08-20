# UNION-Based SQL Injection

- **What it is:** A SQL injection can append a second `SELECT` query so database data is returned in the application's normal response.
- **Where to look:** Endpoints whose database query results are reflected into HTTP responses.
- Find an injectable string parameter.
- Determine the number and compatible types of selected columns.
- Append a `UNION SELECT` that retrieves data from another table.

```sql
' UNION SELECT Username, Password FROM Users;-- 
```

- Match the injected query's column count to the original query.
- Inspect the response for values from the injected `SELECT`.
- **False positives / edge cases:** SQL errors without reflected query output are not UNION-based exploitation.
- **Remediation:** Use parameterized queries and least-privilege database accounts.

## Source: Bug Bounty Bootcamp, Ch. 11
