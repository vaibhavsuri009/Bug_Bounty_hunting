# Gobuster API Directory Enumeration

- What it is: Gobuster brute-forces candidate API paths and reports status codes.
- Use an API-focused wordlist for faster, higher-signal discovery.
```bash
gobuster dir -u http://TARGET:8000 -w /home/hapihacker/api/wordlists/common_apis_160
```
- Investigate hits such as `/api`, `/admin`, `/login`, and `/register`.
- Use `gobuster dir -h` for options.
- The book notes `-b` for ignored status codes and `-x` for additional status handling.
- False positive: wildcard/soft-404 behavior can create convincing fake paths.
- Edge case: GET-only discovery can miss endpoints that exist only for POST/PUT/DELETE.
- Remediation: protect every route with authentication/authorization regardless of discoverability.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
