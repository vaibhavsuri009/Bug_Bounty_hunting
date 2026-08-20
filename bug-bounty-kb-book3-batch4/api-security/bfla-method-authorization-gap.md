# BFLA via HTTP Method Authorization Gap

- What it is: An endpoint can correctly protect one HTTP method while leaving another privileged method exposed.
- Where to look / how to identify it:
  - Capture a legitimate privileged request and test equivalent POST/PUT/PATCH/DELETE methods with a low-privileged controlled token; compare actual effects.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Method acceptance can still lead to a no-op or generic handler.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply consistent authorization per route and method.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
