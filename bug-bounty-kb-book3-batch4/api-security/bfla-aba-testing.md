# A-B-A Testing for BFLA

- What it is: A-B-A testing verifies whether UserB can alter UserA's resource and whether A observes the change.
- Where to look / how to identify it:
  - Create/read a controlled resource as A; use B's token with GET/POST/PUT/DELETE against A's resource; then return to A and verify the server-side effect.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Avoid destructive methods on real data; use test resources only.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Authorize every state-changing action against object ownership and role.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
