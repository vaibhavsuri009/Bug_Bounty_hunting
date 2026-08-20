# GraphiQL Cookie Feature Toggle

- What it is: A client-controlled feature flag may expose a GraphQL IDE or documentation that was intended to be disabled.
- Where to look / how to identify it:
  - Inspect cookies and browser storage for values such as `graphiql:disable`; decode encoded values before testing.
- Exploitation / test pattern:
  - On an authorized lab, change only the feature-toggle value, re-encode it in the original format, and reload the IDE.
- Tools + exact CLI syntax (if mentioned):
  - Burp Decoder: base64-decode the cookie, modify the value, then base64-encode it again.
- Common false-positive / WAF / edge-case notes:
  - The IDE itself is not necessarily a vulnerability; the impact comes from exposed schema, privileged functions, or sensitive operations.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep feature authorization server-side; do not trust client cookies to decide whether privileged tooling is accessible.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
