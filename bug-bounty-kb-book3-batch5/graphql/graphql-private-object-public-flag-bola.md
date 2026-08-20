# GraphQL Private Object Exposure via BOLA

- What it is: A GraphQL response can reveal private objects when an object resolver trusts a caller-supplied identifier.
- Where to look / how to identify it:
  - Compare responses for known public and controlled private objects and inspect fields such as `public:false`.
- Exploitation / test pattern:
  - Keep the caller token constant while switching only the object identifier to prove missing authorization.
- Tools + exact CLI syntax (if mentioned):
  - Use Repeater for confirmation after any enumeration hint.
- Common false-positive / WAF / edge-case notes:
  - Do not treat intentionally shared resources as private; prove the expected access boundary first.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Bind object lookup to the authenticated principal and reject cross-user access.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
