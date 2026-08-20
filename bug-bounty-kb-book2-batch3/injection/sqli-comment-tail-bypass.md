# SQLi Comment-Out Query Tail

- What it is: A SQL comment terminates the application-supplied remainder of a vulnerable query.
- Use only after a quote/Boolean probe indicates likely SQL injection.
- The book's MySQL pattern is:
```text
test' OR 1='1;-- 
```
- The semicolon ends the statement and `-- ` comments out the remaining SQL.
- MySQL requires whitespace after `--`.
- This can neutralize later password or filter conditions appended by the application.
- False positive: DBMS comment syntax differs; failure may mean the wrong database dialect.
- Edge case: stacked statements may be disabled even when comments work.
- Remediation: parameterize every user-controlled value and avoid dynamic SQL construction.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
