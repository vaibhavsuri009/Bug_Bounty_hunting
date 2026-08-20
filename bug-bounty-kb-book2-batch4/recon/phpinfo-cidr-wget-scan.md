# CIDR Scan for Exposed `phpinfo.php`

- What it is: WHOIS-discovered target IP space is checked for a known diagnostic file exposing PHP/server configuration.
- Resolve a target hostname, then use WHOIS to identify an explicitly in-scope netblock.
- The book's shell-loop pattern uses `wget` with one retry and a five-second timeout.
```bash
for ipa in 98.13{6..9}.{0..255}.{0..255}; do
  wget -t 1 -T 5 http://${ipa}/phpinfo.php
done &
```
- Run broad scans only when the bounty scope explicitly permits the IP range.
- False positive: a generic page named `phpinfo.php` may not execute PHP's `phpinfo()`.
- Edge case: scanning hundreds of thousands of IPs can violate rate/scope rules.
- Remediation: remove diagnostic endpoints from production and restrict infrastructure exposure.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
