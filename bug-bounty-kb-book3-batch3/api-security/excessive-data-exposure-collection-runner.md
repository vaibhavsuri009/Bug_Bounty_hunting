# Excessive Data Exposure with Collection Runner

- What it is: API responses may return sensitive fields the caller did not request.
- Where to look / how to identify it:
  - Run legitimate controlled requests; inspect raw JSON for user IDs, emails, vehicle IDs, admin/MFA flags and nested objects beyond UI needs.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Extra harmless metadata may not be a security issue.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Server-side response allowlists should return only needed fields.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
