# InQL Schema and Operation Mapping

- What it is: InQL can turn an exposed GraphQL endpoint/schema into query and mutation templates for testing.
- Where to look / how to identify it:
  - Load the authorized GraphQL endpoint into InQL and inspect generated query/mutation files.
- Exploitation / test pattern:
  - Send interesting generated operations to Repeater and validate them manually.
- Tools + exact CLI syntax (if mentioned):
  - Burp Suite extension: InQL Scanner.
- Common false-positive / WAF / edge-case notes:
  - Generated operations may fail because of required variables or authorization; this is normal.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Protect introspection and enforce authorization independently of client tooling.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
