# Save API Authentication Tokens as Variables

- What it is: Reusable token variables speed authenticated API testing.
- Where to look / how to identify it:
  - Save a successful token/API key as a Postman environment/collection variable; apply as Bearer or `x-access-token`; also save the auth request to regenerate expired tokens.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Tokens can expire or have endpoint-specific scopes.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use short-lived scoped tokens and reliable revocation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
