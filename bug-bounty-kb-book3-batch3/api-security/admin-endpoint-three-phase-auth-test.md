# Three-Phase Administrative Endpoint Authorization Test

- What it is: Admin actions should be tested unauthenticated, low-privileged, then administrative.
- Where to look / how to identify it:
  - Use docs/specs to identify user-management, token, log, enable/disable and group endpoints; compare status/body and actual effect at each privilege level.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A `200` may contain an app-level denial; methods may differ.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Enforce role/function authorization per endpoint and method.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
