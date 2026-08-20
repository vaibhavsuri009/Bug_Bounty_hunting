# IDOR HTTP Method Switch Bypass

- **What it is:** Access control may be enforced for one HTTP method but omitted for another on the same resource.
- **Where to look:** Endpoints supporting GET, POST, PUT, PATCH, or DELETE variants.
- Capture a protected request using one method.
- Keep the same resource reference but try another supported method.

```http
GET /uploads/user1236-01.jpeg
DELETE /uploads/user1236-01.jpeg
```

- Also try converting body parameters into query parameters when switching POST to GET.

```http
GET /get_receipt?receipt_id=2983
```

- Verify effects only against your victim test account.
- **False positives / edge cases:** Different methods may intentionally expose different public operations; confirm unauthorized object access or modification.
- **Remediation:** Centralize authorization so every HTTP method uses the same object-level policy.

## Source: Bug Bounty Bootcamp, Ch. 10
