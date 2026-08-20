# WAF Payload Encoding Test

- What it is: URL/HTML/Base64 or double encoding can create decoding mismatches between a WAF and backend.
- Where to look / how to identify it:
  - Use Burp Decoder to encode only blocked characters first; compare single and double encoding where the application legitimately performs multiple decoding stages.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Successful transport is not impact unless the backend interprets the decoded payload.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize before validation and reject ambiguous/double-encoded input.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
