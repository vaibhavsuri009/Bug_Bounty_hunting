# JWT HMAC Secret Dictionary Crack

- What it is: Weak HS256/HS512 signing secrets can be recovered offline.
- Where to look / how to identify it:
  - Build a target-aware wordlist; `jwt_tool <JWT_TOKEN> -C -d /wordlist.txt`; if recovered, prove impact with a minimally modified controlled token.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - No dictionary hit does not prove adequate key strength.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use long random HMAC secrets and rotate exposed keys.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
