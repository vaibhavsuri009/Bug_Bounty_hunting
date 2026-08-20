# Blind SSRF Timing-Based Port Scan

- What it is: Open/closed/filtered internal ports produce different response times or errors through a blind SSRF.
- First confirm a private host can be reached through the SSRF.
- Test a small set of common ports.
```text
http://127.0.0.1:22/
http://127.0.0.1:80/
http://127.0.0.1:443/
http://127.0.0.1:8080/
http://127.0.0.1:8443/
```
- Compare timing and error messages across repeated requests.
- False positive: proxy timeouts/load balancing can create misleading latency.
- Edge case: an HTTP client speaking to SSH may produce distinctive protocol/header errors.
- Remediation: block private destinations and enforce egress ACLs from the fetcher.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
