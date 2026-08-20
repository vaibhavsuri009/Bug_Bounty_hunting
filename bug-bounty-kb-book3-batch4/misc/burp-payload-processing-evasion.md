# Burp Intruder Payload Processing for Evasion

- What it is: Intruder can apply encoding/prefix/suffix rules to every fuzz payload after a bypass pattern is understood.
- Where to look / how to identify it:
  - Payload Processing rules execute top-to-bottom; book example: URL-encode all characters, then Add Prefix `%00`, then Add Suffix `%00`; inspect the Payload column to verify transformation.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Wrong rule order can encode delimiters unintentionally.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize inbound data before security inspection.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
