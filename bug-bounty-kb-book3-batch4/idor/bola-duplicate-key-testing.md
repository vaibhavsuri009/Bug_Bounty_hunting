# BOLA via Duplicate JSON Keys

- What it is: Repeated object keys may be interpreted differently by validators and backend parsers.
- Where to look / how to identify it:
  - On a controlled request, duplicate an object-ID key with different values and observe which value security controls and business logic use.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - JSON duplicate-key behavior is parser-specific; acceptance alone is not impact.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reject duplicate keys and authorize the canonical parsed value.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
