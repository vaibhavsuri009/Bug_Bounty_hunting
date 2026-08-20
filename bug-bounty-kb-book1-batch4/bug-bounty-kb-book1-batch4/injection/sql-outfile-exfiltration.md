# SQL Injection OUTFILE Exfiltration

- **What it is:** On permissive MySQL deployments, injected SQL may write query results into a server-side file that is later retrievable over HTTP.
- **Where to look:** Confirmed MySQL injection where the database account has file-write privileges and the web root is known.
- The book demonstrates `SELECT ... INTO OUTFILE` for controlled proof of query execution.

```sql
SELECT Password FROM Users WHERE Username='admin'
INTO OUTFILE '/var/www/html/output.txt';
```

- If the server permits the write, request the generated file through the web server.
- This technique can also expose delayed/second-order injection execution.
- **False positives / edge cases:** Modern database accounts commonly lack filesystem write permissions; failure does not mean SQL injection is absent.
- **Remediation:** Parameterize queries and run the database under least privilege without unnecessary filesystem write access.

## Source: Bug Bounty Bootcamp, Ch. 11
