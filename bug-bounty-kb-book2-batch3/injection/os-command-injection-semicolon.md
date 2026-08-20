# OS Command Injection via Semicolon

- What it is: User input is interpolated into a shell command and can append another command.
- Look for ping, traceroute, DNS, conversion, archive, or other system-command-backed features.
- The book's conceptual probe:
```text
google.com;id
```
- Compare output with a normal `google.com` request.
- `id` is useful because it is read-only and shows the process user on Unix-like systems.
- False positive: the application may echo the string without invoking a shell.
- Edge case: escaping may block separators but still leave argument/flag injection.
- Remediation: avoid shells; use safe process APIs with fixed executable and argument arrays.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
