# Rate-Limit User-Agent Rotation Test

- What it is: A weak limiter may include User-Agent in its identity key and reset when the value changes.
- Where to look / how to identify it:
  - After reaching a controlled limit, vary only User-Agent values (SecLists includes User-Agent lists) and observe `x-rate-limit` or success behavior.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Different User-Agent behavior may reflect feature negotiation rather than rate-limit identity.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Rate-limit primarily by authenticated principal and trusted network attributes.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
