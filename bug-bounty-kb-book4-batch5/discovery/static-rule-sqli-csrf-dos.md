# Static SQLi/CSRF/DoS Rule Patterns

- What it is: Static checks can cheaply identify direct query concatenation, state-changing GET routes, and suspicious regex patterns.
- Where to look / how to identify it:
  - Search for user-controlled strings in SQL, mutation logic behind GET, and nested/ambiguous regex used on attacker-controlled input.
- Exploitation / test pattern:
  - Route findings to focused manual review/tests.
- Tools + exact CLI syntax (if mentioned):
  - SAST or grep-like source rules.
- Common false-positive / WAF / edge-case notes:
  - Framework abstractions can make naive rules inaccurate.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce secure query APIs, correct HTTP semantics, and safe regex patterns centrally.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 26
