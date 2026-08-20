# OAuth-Like Redirect Bypass via URL Userinfo Parsing

- What it is: Validation and decoding disagree about whether `@host` is path/userinfo or the final redirect host.
- Test redirect parameters such as `wreply` with encoded slashes and `@`.
- The book's Microsoft pattern involved a double-encoded slash before `@attacker`.
```text
https%3a%2f%2fallowed.example%252f@attacker.example
```
- Observe differences between validation errors and the final redirect target.
- Validate with a controlled test account only.
- False positive: the application may normalize correctly before performing the final redirect.
- Edge case: recursive decoding order is central to this class.
- Remediation: canonicalize once, parse with one URL parser, then exact-match the resulting origin/path.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 17
