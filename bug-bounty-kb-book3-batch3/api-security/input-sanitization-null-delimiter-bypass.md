# Input Sanitization Bypass with Delimiter + Payload

- What it is: A validator may accept a legitimate prefix but mishandle a delimiter plus appended content.
- Where to look / how to identify it:
  - Start with valid input; try `a@b.com%00PAYLOAD`; separately test pipe, quotes, spaces and other delimiters; optionally use two Intruder positions for delimiter and payload.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Validation bypass is not impact unless downstream processing is unsafe.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Canonicalize first, validate the entire value, then process safely.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
