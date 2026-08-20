# BOLA Resource-ID Location Testing

- What it is: BOLA can exist anywhere an API uses a client-controlled identifier to retrieve an object.
- Where to look / how to identify it:
  - Inspect URL paths, query strings, JSON/form bodies and headers for user IDs, resource IDs, organization IDs, emails, phones, addresses, tokens or encoded IDs; swap only with IDs from controlled accounts.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Predictable IDs alone are not BOLA; unauthorized access must actually occur.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Authorize the authenticated principal against the requested object on every request.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
