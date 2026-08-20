# SSRF DNS Resolution Bypass

- Hostname-based SSRF validation can fail when an attacker-controlled domain resolves to an internal IP.
- Configure an `A` or `AAAA` record for a domain you control to point at a restricted address such as `127.0.0.1`.
- Check DNS records with the commands given in the chapter:
```bash
nslookup DOMAIN
nslookup DOMAIN -type=AAAA
```
- Submit the attacker-controlled hostname instead of the literal internal IP:
```text
https://public.example.com/proxy?url=https://attacker.example
```
- If validation trusts the hostname but the fetcher resolves it internally, the server may connect to the blocked destination.
- False-positive trap: secure systems resolve first, verify the resulting IP, and protect against DNS changes between validation and connection.
- Remediation: validate resolved IPs immediately before connection and revalidate after redirects/resolution changes.
## Source: Bug Bounty Bootcamp, Ch. 13
