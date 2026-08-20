# Leaked ID Chaining

- **What it is:** A protected-looking object ID becomes exploitable when another endpoint leaks the supposedly secret reference.
- **Where to look:** Public profiles, list APIs, search endpoints, metadata endpoints, GraphQL, and REST responses.
- Find a sensitive endpoint that uses an opaque object reference.

```http
GET /messages?conversation_id=OPAQUE_ID
```

- Search the application for another endpoint that exposes that reference from a public or low-privilege identifier.

```http
GET /messages?user_id=1236
```

- Use the leaked object ID against the sensitive endpoint with your attacker session.
- **False positives / edge cases:** The leak matters only if the second endpoint fails authorization when the leaked ID is reused.
- **Remediation:** Do not rely on secrecy of object IDs; enforce access control at the sensitive endpoint.

## Source: Bug Bounty Bootcamp, Ch. 10
