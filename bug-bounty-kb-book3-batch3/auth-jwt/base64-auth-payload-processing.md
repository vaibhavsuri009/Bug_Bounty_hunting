# Base64 Authentication Payload Processing in Intruder

- What it is: Base64 auth fields must be re-encoded after fuzz substitution.
- Where to look / how to identify it:
  - Decode the captured value first; mark field; load plaintext payloads; Payload Processing → Encode → Base64.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Base64 is encoding, not security; some formats encode combined `user:password`.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use TLS and robust authentication controls.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
