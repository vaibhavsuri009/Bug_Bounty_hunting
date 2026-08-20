# Deep Fuzzing with Burp Intruder Sniper

- What it is: Cycle one payload list through every selected field of one request.
- Where to look / how to identify it:
  - Proxy a known-good request into Burp; mark headers/path/query/body fields; choose Sniper; load focused payloads; sort status/length and inspect anomalies.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Optional fields may legitimately change response size.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Validate type, length, format and authorization per field.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
