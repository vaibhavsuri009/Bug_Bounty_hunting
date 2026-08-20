# Time-Based Blind SQL Injection

- **What it is:** SQL execution is inferred from a deliberate response delay when a tested database condition is true.
- **Where to look:** Injection points with no useful content or error difference in the HTTP response.
- Establish the normal response-time baseline.
- Inject a condition that calls a database delay function only when true.

```sql
IF(SUBSTR(Password,1,1)='a', SLEEP(10), 0)
```

- Compare repeated true/false test timings.
- Iterate character positions only after confirming the timing signal is consistent.
- **Tools:** Burp Repeater or equivalent manual request replay is useful for timing comparisons.
- **False positives / edge cases:** Network latency and server load can mimic timing differences; repeat both control and test requests.
- **Remediation:** Parameterized queries prevent injected delay functions from becoming executable SQL.

## Source: Bug Bounty Bootcamp, Ch. 11
