# Kiterunner Multi-Method API Scan

- What it is: Kiterunner discovers API routes using realistic methods and route structures, not GET-only directory guessing.
- Run a scan with a `.kite` route set:
```bash
kr scan http://TARGET:8090 -w ~/api/wordlists/data/kiterunner/routes-large.kite
```
- Review unique responses for API docs, events, transaction routes, and other structured paths.
- Use `kr brute <target> -w <wordlist.txt>` when working from a text wordlist.
- Kiterunner can try GET, POST, PUT, and DELETE as appropriate to the route pattern.
- False positive: generic framework handlers can answer many nonexistent routes.
- Edge case: unauthenticated scans may only expose error signatures for protected endpoints.
- Remediation: secure every method/path combination and remove obsolete routes.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
