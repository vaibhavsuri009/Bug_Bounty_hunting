# Authenticated Kiterunner Scan

- What it is: Adding a valid auth header reveals routes hidden from anonymous scans.
- Where to look / how to identify it:
  - `kr scan http://TARGET:8090 -w ~/api/wordlists/data/kiterunner/routes-large.kite -H 'x-access-token: TOKEN'`; compare against unauthenticated output.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - 200 responses can still be generic authenticated errors.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Authorize every route and HTTP method.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
