# SQL Injection Single-Quote Probe

- **What it is:** A single quote is a lightweight probe for inputs that may be embedded unsafely in SQL string literals.
- **Where to look:** Any user-controlled query, form, cookie, header, path, or JSON value that could reach a database query.
- Insert a single quote into one parameter at a time.

```text
'
```

- Compare the response with the baseline request.
- Look for database errors, changed page logic, different status codes, or other anomalies.
- Follow up with database-appropriate payloads that create a clear true/false, time, or response difference.
- **Tools:** A proxy such as Burp is useful for systematically modifying parameters.
- **False positives / edge cases:** Input validation errors or generic 500s can occur for reasons unrelated to SQL parsing.
- **Remediation:** Parameterized queries should cause the quote to be handled only as data.

## Source: Bug Bounty Bootcamp, Ch. 11
