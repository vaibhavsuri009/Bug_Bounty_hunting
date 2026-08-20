# Plain-HTTP API Token Leak Check

- What it is: Tokens can leak if an API accepts sensitive requests over HTTP.
- Where to look / how to identify it:
  - Using only your own traffic, test plain HTTP and inspect URL/header/body data in Wireshark or a proxy; pay special attention to secrets in query/path.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Redirect-before-send may prevent actual leakage.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Force HTTPS/HSTS and never put secrets in URLs.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
