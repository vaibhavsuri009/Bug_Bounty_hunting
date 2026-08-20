# GraphQL Null-Token Authorization Check

- What it is: Some GraphQL resolvers may mishandle empty or null access-token fields and process the request anyway.
- Where to look / how to identify it:
  - Compare a valid token request with missing, empty, and null token variants against controlled private resources.
- Exploitation / test pattern:
  - Confirm whether authorization is genuinely skipped rather than the endpoint being public by design.
- Tools + exact CLI syntax (if mentioned):
  - Postman/Burp Repeater.
- Common false-positive / WAF / edge-case notes:
  - A null token accepted on public data is not a vulnerability.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reject absent/empty credentials consistently and apply resolver-level authorization.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
