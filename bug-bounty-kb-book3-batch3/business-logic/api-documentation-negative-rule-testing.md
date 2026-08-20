# Business Logic Testing from Documentation Warnings

- What it is: Documentation warnings can reveal server-side rules that may be unenforced.
- Where to look / how to identify it:
  - Find 'do not', unsupported value, file type, size or workflow restrictions; reproduce normal flow then test the opposite behavior within scope.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A product recommendation is not automatically a security boundary.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Enforce business rules server-side.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
