# JWT `alg:none` Validation Test

- What it is: A broken verifier may accept an unsigned JWT.
- Where to look / how to identify it:
  - Decode a controlled token; modify a harmless claim; set `alg` to `none`; remove signature while keeping structure; JWT_Tool: `jwt_tool <JWT_TOKEN> -X a`.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Editing a JWT is not impact unless the server accepts it.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Allowlist expected algorithms and require valid signatures.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
