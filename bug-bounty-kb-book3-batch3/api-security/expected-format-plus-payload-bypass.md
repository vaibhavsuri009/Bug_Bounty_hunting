# Expected-Format + Payload Validation Bypass

- What it is: A validator may accept a valid-looking prefix but mishandle appended data.
- Where to look / how to identify it:
  - For a restricted email-like field, keep a valid prefix then append a harmless fuzz marker; if needed test one delimiter/null at a time; compare with invalid-format baseline.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Acceptance alone does not prove a dangerous sink.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Canonicalize and validate the complete value.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
