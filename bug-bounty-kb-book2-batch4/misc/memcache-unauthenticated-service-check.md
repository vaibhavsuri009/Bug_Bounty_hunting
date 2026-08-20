# Unauthenticated Memcache Service Check

- What it is: A publicly reachable Memcache service accepts commands without authentication.
- Discover the port through authorized service scanning.
- Connect with Netcat to the identified Memcache port.
- Run only harmless commands such as `version` and `stats`.
```text
version
stats
```
- Public reachability alone is a red flag because Memcache is normally intended for internal use.
- Do not dump cached keys/data unless the program explicitly permits it.
- False positive: a TCP connection does not prove Memcache command access.
- Edge case: network ACLs may allow only specific source ranges.
- Remediation: bind Memcache privately and restrict access with host/network firewalls.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
