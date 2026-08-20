# NoSQL Operator Authentication Bypass

- What it is: NoSQL query operators can alter authentication predicates when user JSON is inserted directly into a query.
- Where to look / how to identify it:
  - For a controlled account, replace a scalar login value with nested operators such as `{"$gt":""}` or `{"$ne":""}` and compare with the invalid-password baseline.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A parser error does not prove DB execution; operator syntax is database-specific.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce scalar types and construct queries without merging raw client objects.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
