# Blind XXE Out-of-Band Detection

- What it is: Blind XXE may execute without returning data; a controlled external callback can prove the parser resolved an external entity.
- Where to look / how to identify it:
  - Use an authorized callback domain/server and a unique harmless resource reference.
- Exploitation / test pattern:
  - Confirm only that the target fetched the unique test resource; do not exfiltrate sensitive files.
- Tools + exact CLI syntax (if mentioned):
  - HTTP/DNS callback logging in a controlled environment.
- Common false-positive / WAF / edge-case notes:
  - Background services may fetch URLs for unrelated reasons; correlate unique tokens and timing.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable external network resolution from XML parsers and restrict egress.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
