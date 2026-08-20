# Wfuzz JSON Login Brute-Force Pattern

- What it is: Wfuzz can replace a JSON password field with a wordlist.
- Where to look / how to identify it:
  - `wfuzz -d '{"email":"a@email.com","password":"FUZZ"}' --hc 405 -H 'Content-Type: application/json' -z file,/home/hapihacker/rockyou.txt http://TARGET:8888/api/v2/auth`; validate anomalous responses.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A `200` can still mean invalid credentials; rate limits distort results.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: MFA, rate limiting and credential-stuffing detection.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
