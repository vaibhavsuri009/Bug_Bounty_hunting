# Mass Assignment Variable Mining from Documentation

- What it is: Privileged request examples reveal hidden model property names usable in lower-privilege endpoints.
- Where to look / how to identify it:
  - Compare standard-user and admin create/update examples; extract fields such as `admin`, role, org, credit or MFA state; test one field at a time on a controlled low-privilege request.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A field name can exist but be ignored on the tested endpoint.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use endpoint-specific writable-property allowlists.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
