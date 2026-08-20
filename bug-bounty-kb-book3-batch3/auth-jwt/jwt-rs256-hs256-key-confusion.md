# JWT RS256-to-HS256 Key Confusion

- What it is: A verifier may accept HS256 and misuse an RSA public key as the HMAC secret.
- Where to look / how to identify it:
  - Prereqs: RS256 target, HS256 accepted, public key known; `jwt_tool <JWT_TOKEN> -X k -pk public-key.pem`; validate only with controlled claims.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Patched libraries reject this; key format matters.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Pin the algorithm and separate asymmetric/symmetric key handling.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
