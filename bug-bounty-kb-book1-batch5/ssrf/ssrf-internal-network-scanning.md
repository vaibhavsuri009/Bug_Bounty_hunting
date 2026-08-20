# SSRF Internal Network Scanning

- Use a confirmed SSRF to identify reachable internal hosts by varying private IP addresses.
- Keep the request identical except for the destination host.
```http
POST /upload_profile_from_url
user_id=1234&url=https://10.0.0.1
```
- Compare with adjacent addresses such as `10.0.0.2`.
- Service banners, HTTP content, status codes, connection errors, and timing differences can reveal which hosts exist.
- Record only clearly distinguishable host behavior; do not treat one timeout as proof.
- Tools: Burp Repeater; SSRFmap is mentioned for automated SSRF testing.
- False-positive trap: load balancers, proxies, and generic error handlers can make unrelated hosts look identical.
- Remediation: deny arbitrary internal connectivity from public-facing fetch features and segment network privileges.
## Source: Bug Bounty Bootcamp, Ch. 13
