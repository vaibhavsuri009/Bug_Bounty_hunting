# API Documentation Path Discovery

- What it is: Docs expose endpoints/methods/params/auth/admin actions.
- Where to look / how to identify it:
  - Try `/docs`, `/api/docs`, `docs.example.com`, `dev.example.com/docs`, `api.example.com/docs`; also authenticated developer areas, directory brute force, search engines, and Wayback.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Archived docs may be stale; always test undocumented behavior too.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Keep docs current and avoid exposing unnecessary admin internals.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
