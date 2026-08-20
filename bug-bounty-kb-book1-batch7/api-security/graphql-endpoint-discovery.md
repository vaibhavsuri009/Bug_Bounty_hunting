# GraphQL: Endpoint Discovery

- **What it is:** Identify GraphQL interfaces before schema enumeration and authorization testing.
- **Common paths mentioned:** `/graphql`, `/gql`, and `/g`.
- **Where to look:** Web/mobile API calls, JavaScript, developer docs, error responses, and proxy history.
- **Method:** Probe likely endpoints with a harmless GraphQL query and observe whether GraphQL-formatted errors/data return.
- **Edge case:** Some applications use versioned or custom GraphQL paths.
- **False positives:** A JSON endpoint that accepts POST does not prove GraphQL; confirm GraphQL query parsing.
- **Remediation:** Treat GraphQL as an exposed API surface and enforce authentication/authorization on every resolver.

```graphql
query {
  __typename
}
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
