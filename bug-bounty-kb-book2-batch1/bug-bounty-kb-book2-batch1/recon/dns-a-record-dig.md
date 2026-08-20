# DNS A-Record Lookup with dig

- What it is: Resolve a target domain to its IPv4 address during reconnaissance.
- Where to look: Any in-scope hostname or subdomain whose underlying server address matters.
- Query the domain directly from a terminal:
```bash
dig A site.com
```
- Replace `site.com` with the hostname you are investigating.
- Record returned IP addresses and correlate them with other discovered assets.
- Re-run against newly discovered subdomains rather than assuming they share infrastructure.
- Tools: `dig` / DNS resolver.
- False-positive trap: An IP may belong to shared hosting, a CDN, or another intermediary; resolution alone does not prove asset ownership.
- Remediation: Not a vulnerability by itself; use appropriate DNS/CDN architecture when origin exposure is a concern.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 1
