# GraphQL Endpoint Wordlist Discovery

- What it is: GraphQL commonly uses a single endpoint, so path discovery is a high-value reconnaissance step.
- Where to look / how to identify it:
  - Try likely paths such as `/graphql`, `/v1/graphql`, `/api/graphql`, `/graphiql`, `/playground`, `/altair`, `/console`, and version/path variants.
- Exploitation / test pattern:
  - Use API-aware directory brute forcing and treat unique non-404 responses as candidates.
- Tools + exact CLI syntax (if mentioned):
  - `kr brute http://TARGET -w /usr/share/seclists/Discovery/Web-Content/graphql.txt`
- Common false-positive / WAF / edge-case notes:
  - A `400` can still prove an endpoint exists; inspect the body before discarding it.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Do not expose GraphQL IDEs unnecessarily; restrict access and return consistent errors.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
