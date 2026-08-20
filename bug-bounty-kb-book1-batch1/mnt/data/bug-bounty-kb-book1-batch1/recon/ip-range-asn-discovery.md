# IP Range and ASN Discovery

- What it is: Map domains to IPs, ranges, and autonomous systems to identify organization-owned infrastructure.
- Resolve a known domain:
```bash
nslookup example.com
```
- Run WHOIS on a discovered IP and inspect `NetRange`, `CIDR`, and organization fields:
```bash
whois 157.240.2.35
```
- Translate IPs to ASNs with Team Cymru WHOIS:
```bash
whois -h whois.cymru.com 157.240.2.35
```
- Repeat for several nearby IPs; consistent ASN ownership can indicate a dedicated range.
- Use reverse-IP services to find other domains hosted on the same server/IP.
- Only treat newly identified IPs as attackable after scope confirmation.
- False-positive trap: shared hosting/CDNs can place unrelated domains on one IP or ASN.
- Remediation: N/A — infrastructure reconnaissance.

## Source: Bug Bounty Bootcamp, Ch. 5
