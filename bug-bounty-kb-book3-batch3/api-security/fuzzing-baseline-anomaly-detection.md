# Fuzzing Baseline and Anomaly Detection

- What it is: A stable baseline makes rare fuzz-response differences visible.
- Where to look / how to identify it:
  - Send expected/invalid controls; record status, length, body and timing; sort results; use Burp Comparer + Sync Views for small differences.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Dynamic timestamps/session IDs can create harmless diffs.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use uniform validation/error behavior.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
