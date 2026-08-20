# JWT_Tool Playbook Scan

- What it is: JWT_Tool can automate common JWT weakness checks.
- Where to look / how to identify it:
  - `jwt_tool -t http://target-site.com/ -rc "Header: JWT_Token" -M pb`; replace the header name/token and manually validate findings.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Automated success detection can be wrong.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Pin algorithms and validate signature, issuer, audience and expiry.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
