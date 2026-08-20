# GraphQL: Enumerate Fields with __type

- **What it is:** Query a known GraphQL type to enumerate its fields for follow-on testing.
- **Where to look:** Type names discovered through introspection or application queries.
- **Core field:** `__type(name: "customer")` returns metadata about a type.
- **Method:** Enumerate fields, identify IDs/private attributes, then construct read or mutation tests around them.
- **False positives:** Schema visibility does not imply the current user can access every field.
- **Edge case:** Field-level authorization may differ from object-level authorization.
- **Remediation:** Enforce authorization at resolver/field level for sensitive properties.

```graphql
{
  __type(name: "customer") {
    name
    fields { name }
  }
}
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
