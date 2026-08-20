# WAF/Input-Filter String Terminator Test

- What it is: Nulls and delimiter characters can expose canonicalization differences between filters and backend parsers.
- Where to look / how to identify it:
  - Test one delimiter at a time around a harmless payload: `%00`, `0x00`, `//`, `;`, `%`, `!`, `?`, `[]`, `%09`, `%0a`, etc.; compare whether filtering and backend interpretation diverge.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Different encodings may be rejected before reaching the application.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize once before validation and use the same parsed value downstream.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
