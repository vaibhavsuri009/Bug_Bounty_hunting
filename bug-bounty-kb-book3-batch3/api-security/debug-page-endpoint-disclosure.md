# Debug Page Endpoint Disclosure

- What it is: Verbose debug pages can expose route tables, stack traces and framework details.
- Where to look / how to identify it:
  - Request a harmless nonexistent route/malformed input; inspect 404/500 output for endpoints and implementation details; use them only as discovery leads.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Custom errors can resemble framework debug pages.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Disable debug mode and verbose traces outside isolated dev.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
