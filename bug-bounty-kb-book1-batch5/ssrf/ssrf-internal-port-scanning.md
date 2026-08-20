# SSRF Internal Port Scanning

- After finding an internal host, vary its port to fingerprint reachable services.
- Ports range from `0` to `65535`; common examples in the chapter include SSH `22`, HTTP `80`, HTTPS `443`.
```text
https://10.0.0.1:80
https://10.0.0.1:11
```
- Compare banners, connection failures, status codes, and response times.
- A returned server banner can reveal service/version information useful for further authorized testing.
- Keep host constant while changing only the port to reduce ambiguity.
- Tools: Burp Repeater; SSRFmap is mentioned for automation.
- False-positive trap: a proxy may normalize errors or block non-HTTP protocols, hiding true port state.
- Remediation: restrict fetchers to required schemes, destinations, and ports only.
## Source: Bug Bounty Bootcamp, Ch. 13
