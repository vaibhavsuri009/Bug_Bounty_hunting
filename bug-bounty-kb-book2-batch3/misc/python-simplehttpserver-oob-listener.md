# Python SimpleHTTPServer as XXE Callback Listener

- What it is: A minimal HTTP server records external-entity callbacks during authorized testing.
- The book uses Python's legacy SimpleHTTPServer module.
```bash
sudo python -m SimpleHTTPServer 80
```
- Place the external DTD in the served directory when testing remote-DTD resolution.
- Watch request paths for unique XXE tokens or callback parameters.
- A request for the DTD confirms remote retrieval by the target parser.
- False positive: unrelated crawlers may request the file; use unique unguessable paths.
- Edge case: modern Python uses `python3 -m http.server 80`, but the book specifically shows the legacy command.
- Remediation note: this is a testing utility; fix the target by disabling external entities.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 11
