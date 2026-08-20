# Generic API Fuzz Input Set

- What it is: Malformed values reveal weak validation/error handling.
- Where to look / how to identify it:
  - Test one field at a time using huge numbers, long strings, Unicode, symbols, nulls and targeted strings such as `%00`, `0x00`, `$ne`, `$gt`, `|whoami`, `' OR 1=1-- -`; compare to baseline.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Verbose errors may disclose tech without direct exploitability.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Strict schema/type validation and safe errors.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
