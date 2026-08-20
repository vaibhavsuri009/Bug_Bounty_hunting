# Side-Channel BOLA Enumeration

- What it is: Timing, status-code or response-length differences can reveal whether protected resources exist.
- Where to look / how to identify it:
  - Build baselines for nonexistent and known-valid controlled identifiers; compare candidate IDs for stable differences such as `404` vs `405/401`, body length or `X-Response-Time`.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Caching, load and gateways can create unstable side channels.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Normalize unauthorized/nonexistent responses and timing where practical.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
