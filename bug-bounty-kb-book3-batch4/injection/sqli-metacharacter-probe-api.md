# API SQLi Metacharacter Probe

- What it is: SQL metacharacters can reveal that API input reaches SQL syntax unsafely.
- Where to look / how to identify it:
  - Test one database-backed field with paired controls and metacharacters such as `'`, `"`, `--`, `;`, and Boolean conditions like `' OR 1=1-- -`; compare errors/results.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Validation errors may occur before the database; syntax varies by DBMS.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use prepared statements and strict type validation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
