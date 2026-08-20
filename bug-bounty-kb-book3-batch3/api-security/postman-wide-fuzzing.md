# Wide Fuzzing with Postman Collection Runner

- What it is: Apply one fuzz value across many requests to find broad weak points.
- Where to look / how to identify it:
  - Create fuzz variables; replace shared token/path/placeholder; baseline with normal values; rerun one fuzz value at a time; compare failed tests, halted runs and anomalies.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Endpoints may legitimately reject values differently; token-generation requests can overwrite variables.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use consistent validation/auth controls.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
