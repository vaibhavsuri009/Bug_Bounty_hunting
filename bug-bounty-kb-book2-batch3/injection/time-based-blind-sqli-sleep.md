# Time-Based Blind SQLi with `sleep()`

- What it is: Query execution is inferred from a deliberate database delay.
- Useful when content does not differ between true and false queries.
- The book's MySQL-style condition adds:
```text
and sleep(12) = 1
```
- Measure baseline latency first, then compare several delayed requests.
- Keep delays minimal while still distinguishable from network jitter.
- A consistent added delay indicates the injected DB function likely executed.
- False positive: slow backend behavior or rate limiting can mimic a delay.
- Edge case: WAFs often block obvious `sleep()` payloads.
- Remediation: parameterize queries and apply least-privilege DB permissions.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
