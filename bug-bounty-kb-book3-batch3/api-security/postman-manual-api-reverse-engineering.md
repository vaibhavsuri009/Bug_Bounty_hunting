# Manual API Reverse Engineering with Postman

- What it is: Build a collection manually when no usable docs/spec exist.
- Where to look / how to identify it:
  - Create a collection + `baseURL`; add each discovered request with method, headers, params and body; group by endpoint; use a version variable for v1/v2/v3 changes.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Expired tokens/nonces can make copied requests look broken.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Maintain accurate internal specs and repeatable test collections.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
