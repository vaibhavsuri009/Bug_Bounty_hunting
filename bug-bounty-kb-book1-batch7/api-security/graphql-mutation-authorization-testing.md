# GraphQL: Mutation Authorization Testing

- **What it is:** Lower-privileged users can execute a mutation captured from a higher-privileged account.
- **Where to look:** State-changing GraphQL operations that edit/delete/administer objects.
- **Method:** Capture an allowed mutation from account A; replay the same mutation from account B that should lack permission.
- **Vary:** Object IDs, fields, nested input, and requested return fields.
- **Also compare:** GraphQL authorization against equivalent REST/web functionality because controls may differ.
- **False positives:** A mutation may return success-like JSON while silently performing no change; verify state.
- **Remediation:** Apply resolver-level authorization for every mutation and affected object.

```graphql
mutation {
  updateObject(id: "OTHER_USER_ID", input: { /* controlled change */ }) { id }
}
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
