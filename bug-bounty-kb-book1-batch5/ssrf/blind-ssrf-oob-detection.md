# Blind SSRF OOB Detection

- Blind SSRF occurs when the forged request executes but the application does not return the fetched content.
- Point the suspected URL parameter at a host you control and monitor for target-originated connections.
- Prefer a unique path/hostname so callbacks can be correlated to one request.
- Local listener method from the chapter:
```bash
apt-get install netcat
nc -lp 8080
```
- Then submit your reachable IP/hostname with port `8080` as the SSRF destination.
- Burp Suite Pro Collaborator can generate unique callback domains and monitor interactions automatically.
- Confirm more than outbound connectivity: compare access to internal hosts/ports to establish exploitability.
- False-positive trap: generic webhooks may intentionally call arbitrary external URLs; the security impact comes from reaching restricted resources or leaking sensitive request data.
- Remediation: restrict outbound destinations/protocols and enforce network egress controls.
## Source: Bug Bounty Bootcamp, Ch. 13
