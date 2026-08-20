# Error-Based SQL Injection

- **What it is:** The attacker deliberately triggers a database error that includes sensitive query data in the returned error message.
- **Where to look:** Endpoints that expose verbose database errors to the client.
- Confirm that injected SQL executes.
- Force a value into an incompatible conversion or operation.

```sql
UNION SELECT 1,
CONVERT((SELECT Password FROM Users WHERE Username='admin'), DATE);--
```

- Inspect the database error for the value it failed to convert.
- Use controlled data when demonstrating the issue where possible.
- **False positives / edge cases:** A generic 500 response proves only an error, not data extraction.
- **Remediation:** Parameterize queries and suppress detailed database errors from untrusted clients.

## Source: Bug Bounty Bootcamp, Ch. 11
