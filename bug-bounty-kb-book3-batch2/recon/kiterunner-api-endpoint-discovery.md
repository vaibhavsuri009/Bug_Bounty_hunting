# Kiterunner API Endpoint Discovery

- What it is: Kiterunner discovers API resources using API-aware paths, methods, parameters, and headers.
- Install from source:
```bash
git clone https://github.com/assetnote/kiterunner.git
cd kiterunner && make build
sudo ln -s $(pwd)/dist/kr /usr/local/bin/kr
```
- Use `.kite`, Swagger JSON, or text wordlists as discovery input.
- Prefer API-specific wordlists because Kiterunner understands realistic API route structures.
- Review unique status/length responses and replay interesting hits.
- False positive: framework signatures and generic error handlers can look like valid routes.
- Edge case: WAF/rate limits can distort results.
- Remediation: do not expose undocumented routes without equivalent authentication/authorization.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
