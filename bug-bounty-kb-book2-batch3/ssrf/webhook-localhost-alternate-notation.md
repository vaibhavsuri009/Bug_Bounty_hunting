# SSRF Localhost Filter Bypass with Alternate IP Notation

- What it is: A blacklist blocks `localhost`/`127.0.0.1` but misses equivalent loopback forms.
- Use only after direct loopback references are rejected.
- The book mentions shortened alternatives such as:
```text
127.0.1
127.1
```
- Submit these as webhook/import destinations and compare behavior.
- A bypass alone is low impact; demonstrate only authorized internal reachability or response differences.
- False positive: acceptance of the URL without an actual server-side request proves nothing.
- Edge case: URL parsers and language runtimes normalize numeric IP forms differently.
- Remediation: resolve the hostname/IP, canonicalize it, then enforce private-range blocks on the resolved address.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
