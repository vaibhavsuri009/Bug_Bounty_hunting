# CRLF Header Injection Probe

- What it is: `%0D%0A` is decoded into HTTP line breaks inside a response header.
- Look for user-controlled values copied into headers, especially `Set-Cookie` or `Location`.
- Inject a harmless synthetic header marker.
```text
%0D%0AX-Test:%20crlf
```
- Inspect the raw HTTP response to see whether `X-Test: crlf` becomes a separate header.
- Test case-insensitive forms because percent-encoding hex digits are not case-sensitive.
- The book notes `%0A%20` as an Internet Explorer-specific variation.
- False positive: seeing the encoded bytes reflected literally is not CRLF injection.
- Edge case: proxies, frameworks, and browsers may normalize line endings differently.
- Tools: intercepting proxy/raw response viewer.
- Remediation: reject CR/LF in header-bound input and use framework APIs that prevent raw header construction.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 6
