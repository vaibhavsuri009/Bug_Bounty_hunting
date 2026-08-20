# A-B Testing for BOLA

- What it is: A-B testing creates a resource as UserA and attempts to retrieve it using UserB.
- Where to look / how to identify it:
  - Create two controlled users; create a private resource as A; capture the legitimate request; replace A's token with B's while keeping A's resource identifier; compare result.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Public/shared objects can legitimately be accessible by B.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Perform object-level authorization for every read operation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
