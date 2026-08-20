# NoSQL Injection JSON-Boundary Troubleshooting

- What it is: Intruder payload placement or URL encoding can prevent nested JSON injection from reaching the parser correctly.
- Where to look / how to identify it:
  - Inspect the exact sent request; disable automatic URL encoding only when needed; move attack markers to encompass the entire JSON value, e.g. `{"coupon_code":§"TEST!"§}` so object payloads replace the scalar cleanly.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - 422/JSON syntax errors often mean malformed delivery rather than a patched vulnerability.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Validate request schemas and reject operator objects in scalar fields.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
