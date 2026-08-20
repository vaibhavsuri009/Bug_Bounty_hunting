# WAF Case-Switching Test

- What it is: Case-sensitive rules may miss payloads whose keywords use mixed capitalization.
- Where to look / how to identify it:
  - Take a harmless known-blocked pattern and alter keyword case, e.g. mixed-case script/SQL keywords; compare whether the filter behavior changes while backend parsing remains equivalent.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Many modern parsers/WAFs normalize case, so acceptance may not imply exploitability.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Normalize/canonicalize before applying security rules.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
