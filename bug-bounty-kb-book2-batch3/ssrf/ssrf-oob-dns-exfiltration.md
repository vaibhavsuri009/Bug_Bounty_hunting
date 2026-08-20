# Blind SSRF OOB DNS Exfiltration

- What it is: A blind server-side primitive leaks small values through DNS lookups to an attacker-controlled domain.
- Use only where the SSRF or adjacent command primitive can control a lookup hostname.
- Encode data into DNS-safe characters before placing it in a subdomain.
```text
ENCODED_DATA.yourdomain.example
```
- The book notes Base32 for data that contains non-alphanumeric characters.
- Observe authoritative DNS logs for the callback.
- False positive: DNS callbacks can come from scanners/resolvers unrelated to the vulnerable action.
- Edge case: label length and total DNS-name length limit how much data fits per query.
- Remediation: restrict outbound DNS and eliminate the underlying SSRF/command injection.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
