# GraphQL: Enumerate Types with Introspection

- **What it is:** Use GraphQL introspection to learn the API schema when introspection is enabled.
- **Where to look:** Confirmed GraphQL endpoint.
- **Core field:** `__schema` can return available types.
- **Method:** Query schema types, identify interesting objects/mutations, then request fields relevant to authorization or sensitive data.
- **Value:** Introspection can reveal hidden application capabilities faster than endpoint guessing.
- **False positives:** Introspection exposure alone may be informational; impact comes from what the schema enables or discloses.
- **Remediation:** Consider disabling introspection on production and always enforce resolver-level access control.

```graphql
{
  __schema {
    types { name }
  }
}
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
