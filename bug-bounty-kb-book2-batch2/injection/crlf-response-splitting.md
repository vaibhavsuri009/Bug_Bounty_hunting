# CRLF HTTP Response Splitting

- What it is: Injected CRLF sequences terminate one response section and create attacker-controlled headers/body.
- First confirm a controllable value reaches an HTTP response header.
- The book demonstrates a structure that ends the original body and starts another response.
```text
%0d%0aContent-Length:%200%0d%0a%0d%0a
HTTP/1.1%20200%20OK%0d%0a
Content-Type:%20text/html%0d%0a...
```
- Use a harmless marker body when proving the parsing boundary.
- Verify behavior in raw response and browser separately.
- False positive: some clients display malformed bytes without treating them as a second response.
- Edge case: intermediary proxies may normalize or reject the crafted response.
- Potential impact includes cache poisoning, redirect/header injection, or XSS when another sink is available.
- Remediation: prevent CR/LF from entering response headers and canonicalize/validate header values.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 6
