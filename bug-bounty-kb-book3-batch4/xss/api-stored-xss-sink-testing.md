# API-to-Frontend Stored XSS Testing

- What it is: An API may store user input that a browser later renders unsafely.
- Where to look / how to identify it:
  - Target profile fields, likes, product data, forum/comments and similar UI-backed inputs; submit a harmless XSS proof to a controlled object, then load the relevant page to test execution.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A successful API response without browser execution is not XSS.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Contextually encode output and sanitize rich content.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
