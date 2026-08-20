# API: BOLA/IDOR Testing

- **What it is:** Broken object-level authorization where changing a resource/user identifier exposes or modifies another user’s data.
- **Where to look:** IDs in REST paths/query/body, GraphQL arguments, SOAP fields, or leaked IDs from other endpoints.
- **Method:** Use two accounts with different ownership; replay a legitimate request from account A with account B’s object ID.
- **Actions:** Test read, modify, and delete operations—not just GET.
- **If IDs are unpredictable:** Search other API responses for leaked IDs and chain the disclosure.
- **False positives:** Public resources can be readable by design; verify expected ownership/authorization.
- **Remediation:** Authorize every object access using server-side identity and ownership/role checks.

```http
GET /api/resource/ATTACKER_OBJECT
GET /api/resource/OTHER_USERS_OBJECT
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
