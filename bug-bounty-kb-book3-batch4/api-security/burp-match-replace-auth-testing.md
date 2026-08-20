# Burp Match-and-Replace Authorization Testing

- What it is: Burp Match and Replace can replay a browser workflow while automatically substituting another user's token.
- Where to look / how to identify it:
  - Collect UserA requests involving protected resources; configure a request-header rule matching TokenA and replacing it with TokenB; repeat the workflow and investigate unexpected success.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Per-request CSRF/nonces can cause unrelated failures.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Bind every protected action to the current authenticated principal.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
