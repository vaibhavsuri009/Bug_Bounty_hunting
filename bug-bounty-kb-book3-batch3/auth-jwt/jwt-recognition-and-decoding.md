# JWT Recognition and Decoding

- What it is: JWTs normally contain header.payload.signature separated by periods.
- Where to look / how to identify it:
  - Decode with Burp Decoder/jwt.io/JWT_Tool; inspect `alg`, `typ`, user/subject, privilege fields, `iat`, `exp`, `nbf`; remember decoded claims are untrusted until signature checks are verified.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - JWT-like strings can be unrelated test data.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Minimize sensitive claims and validate signature/algorithm/expiry.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
