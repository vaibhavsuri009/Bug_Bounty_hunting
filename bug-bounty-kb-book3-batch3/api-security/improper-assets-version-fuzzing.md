# Improper Assets Management via Version Fuzzing

- What it is: Old/test/dev API versions may remain reachable with weaker security.
- Where to look / how to identify it:
  - Replace version path with a Postman variable; test `v1`, `v2`, `v3`, `test`, `mobile`, `uat`, `dev`, `old`, `internal`; establish nonexistent-path baseline then investigate deviations.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Old paths can simply proxy to current code.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Inventory and fully retire unsupported versions.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
