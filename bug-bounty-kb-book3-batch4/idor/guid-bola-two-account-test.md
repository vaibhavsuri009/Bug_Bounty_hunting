# GUID/UUID BOLA with Two Controlled Accounts

- What it is: Long random GUIDs do not replace authorization; obtain a real second-user GUID instead of brute-forcing.
- Where to look / how to identify it:
  - Create UserB, obtain B's resource GUID through normal use, then request B's resource using UserA's token; compare with expected denial.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Knowledge of a GUID is not itself a flaw if authorization works.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Check ownership server-side regardless of identifier entropy.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
