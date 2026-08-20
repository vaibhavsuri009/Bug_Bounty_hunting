# API Injection Point Mapping

- What it is: Injection can occur in any client-controlled value passed to databases, shells or renderers.
- Where to look / how to identify it:
  - Prioritize API keys, tokens, headers, query strings, POST/PUT parameters, upload fields and inputs that already produced verbose errors; fuzz one field at a time.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A parser error is only a lead, not proof of code/database execution.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate by type/schema and use safe downstream APIs.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
