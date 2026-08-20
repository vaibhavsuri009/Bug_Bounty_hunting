# Build a Postman Collection by Proxy

- What it is: Capture API traffic behind a GUI into a reusable collection.
- Where to look / how to identify it:
  - Enable Capture Requests; use the browser proxy port (book: `5555`); exercise signup/login/reset/profile/forum/shop; remove static/third-party noise and group requests.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Third-party requests may be out of scope; duplicates add noise.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Do not rely on hidden GUI routes for security.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
