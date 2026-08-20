# SSRF into Internal DNS

- What it is: User-controlled DNS-server input makes the target query private DNS infrastructure.
- Look for diagnostic tools that accept a custom nameserver/IP.
- Begin with localhost or RFC1918/private ranges to test reachability.
```text
127.0.0.1
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```
- Distinguish "did not respond" from explicit access-denied validation errors.
- Once a responsive internal DNS server is found, query only authorized internal names.
- False positive: an empty response may simply be a reachable DNS server with no record.
- Edge case: carrier-grade/private ranges can also be relevant depending on the environment.
- Remediation: restrict custom resolver targets to approved public DNS servers.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
