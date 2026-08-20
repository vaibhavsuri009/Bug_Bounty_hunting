# SSRF IPv6 Blocklist Bypass

- IPv4-focused SSRF filters may forget equivalent IPv6 local/private addresses.
- Test IPv6 forms when IPv4 loopback/private destinations are blocked.
- Values highlighted in the chapter:
```text
::1      # localhost
fc00::   # private network range starting point
```
- Place the IPv6 destination into the vulnerable URL input using syntax accepted by the target HTTP client.
- Compare filter decisions for equivalent IPv4 and IPv6 targets.
- A bypass exists when the application rejects the IPv4 form but allows an IPv6 address reaching the same restricted network.
- False-positive trap: some HTTP clients require brackets around literal IPv6 hosts in URLs.
- Remediation: normalize both IPv4 and IPv6 and enforce the same restricted-network policy on both.
## Source: Bug Bounty Bootcamp, Ch. 13
