# Wfuzz: Path Enumeration

- **What it is:** Enumerate hidden files/directories by replacing `FUZZ` with path wordlist entries.
- **Where to use:** Recon against an authorized web target.
- **Command:** `-w` selects wordlist; `-f` writes results; `--hc 404` hides 404s; `--follow` follows redirects.
- **Method:** Use a technology-appropriate path list and investigate surviving 2xx/3xx/interesting responses.
- **Output fields:** Wfuzz reports response code and response lengths alongside the payload.
- **False positives:** Custom 404 pages may return 200; compare response size/body, not status alone.
- **Remediation:** Remove unnecessary endpoints and enforce auth on sensitive paths.

```bash
wfuzz -w wordlist.txt -f output.txt --hc 404 --follow http://example.com/FUZZ
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
