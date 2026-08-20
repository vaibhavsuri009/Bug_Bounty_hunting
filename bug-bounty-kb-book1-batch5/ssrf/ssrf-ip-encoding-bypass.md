# SSRF IP Encoding Bypass

- Blocklists may recognize only the normal decimal representation of internal IP addresses.
- Try alternate representations of loopback addresses supported by the target URL parser.
```text
127.0.0.1              # decimal
0x7f.0x0.0x0.0x1       # hex
0177.0.0.01             # octal
2130706433              # dword
%6c%6f%63%61%6c%68%6f%73%74  # URL-encoded localhost
0177.0.0.0x1            # mixed encoding
```
- Submit variants through the same SSRF parameter and compare filter results.
- The bypass depends on the validator and HTTP client normalizing the address differently.
- False-positive trap: modern parsers may reject unusual numeric forms or canonicalize before validation.
- Remediation: canonicalize hostnames/IPs first, then apply network restrictions to the resolved canonical address.
## Source: Bug Bounty Bootcamp, Ch. 13
