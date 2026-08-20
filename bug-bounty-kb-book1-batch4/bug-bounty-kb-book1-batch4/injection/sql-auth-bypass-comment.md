# SQL Injection Authentication Bypass with Comments

- **What it is:** Unsafely concatenated login input can alter SQL logic and comment out password checks.
- **Where to look:** Login forms and authentication endpoints that pass user input into database queries.
- Probe parameters for SQL parsing behavior first.
- A classic pattern is to terminate the username string and comment out the remaining query.

```text
username=admin';-- 
```

- Conceptual resulting query:

```sql
SELECT Id FROM Users WHERE Username='admin';-- ' AND Password='...';
```

- Confirm only against an authorized test account.
- **False positives / edge cases:** Generic login errors do not prove SQL injection; demonstrate that injected syntax changes authentication logic.
- **Remediation:** Use prepared/parameterized statements; never concatenate raw login input into SQL.

## Source: Bug Bounty Bootcamp, Ch. 11
