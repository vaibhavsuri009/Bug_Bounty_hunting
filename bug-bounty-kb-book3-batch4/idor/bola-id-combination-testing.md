# BOLA ID-Combination Testing

- What it is: Some APIs require both a user/group identifier and a resource identifier, creating multi-ID authorization attack surfaces.
- Where to look / how to identify it:
  - Replay a known-good controlled request while changing the user/group/object combination, e.g. UserA token + UserB/group/resource identifiers.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A successful response may still be intentionally shared data; verify privacy expectations.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate every identifier relationship server-side, not just token validity.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
