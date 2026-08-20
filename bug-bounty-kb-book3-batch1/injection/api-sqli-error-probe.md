# API SQL Injection Error Probe

- What it is: Unsanitized API input reaches a SQL interpreter and changes query syntax.
- Insert SQL metacharacters into a normal string field or query parameter.
- The book shows a Boolean/error-style probe:
```text
' OR 1=0--
```
- Compare status code, body, response time, and verbose database errors against baseline.
- A direct SQL syntax error is a strong injection indicator.
- Confirm with a paired control before escalating.
- False positive: application validators can reject metacharacters without any database interaction.
- Edge case: DBMS-specific syntax/comment rules vary.
- Remediation: parameterized queries plus strict type validation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
