# Postman Collection Token-Swap Authorization Test

- What it is: A collection-level token variable lets you test many requests for BOLA/BFLA efficiently.
- Where to look / how to identify it:
  - Baseline requests with UserA's token; replace the collection auth variable with UserB's; run only private/resource-sensitive requests and flag unexpected successful responses.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Shared/public endpoints will legitimately remain successful.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize object/function authorization consistently across the API.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
