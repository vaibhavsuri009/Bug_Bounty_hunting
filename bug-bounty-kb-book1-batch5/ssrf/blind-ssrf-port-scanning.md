# Blind SSRF Port Scanning

- Use response-code or timing differences from a blind SSRF to infer internal port state.
- Send the same SSRF request repeatedly while changing only the destination port.
```http
POST /webhook
url=https://127.0.0.1:80
```
```http
POST /webhook
url=https://127.0.0.1:11
```
- The chapter example observes `200` for a reachable/open port and `500` for an unavailable port.
- Also compare response time; closed ports may fail quickly while filtered/firewalled destinations may delay.
- Do not assume one universal signature—compare relative behavior among addresses/ports on the same target.
- Tools: Burp Repeater shows response time; SSRFmap is mentioned for automation.
- False-positive trap: uniform status codes, queues, retries, or upstream timeouts can hide port-state differences.
- Remediation: prevent server-side fetchers from connecting to arbitrary internal hosts/ports and restrict egress.
## Source: Bug Bounty Bootcamp, Ch. 13
