# Boolean-Based Blind SQL Injection

- **What it is:** Database contents are inferred by injecting conditions whose true/false result changes observable application behavior.
- **Where to look:** Suspected SQL injection points where query results and database errors are not directly returned.
- Identify a stable response difference tied to a Boolean condition.
- Test one character or fact at a time.

```sql
SUBSTR(Password,1,1)='a'
```

- Wrap the condition in the vulnerable query and compare true versus false responses.
- Iterate over candidate characters to infer the value gradually.
- The observable signal can be a banner, row count, page state, or other deterministic difference.
- **False positives / edge cases:** Dynamic pages can create noisy response differences; repeat tests to establish a reliable oracle.
- **Remediation:** Use parameterized queries and avoid exposing query-dependent behavioral side channels.

## Source: Bug Bounty Bootcamp, Ch. 11
