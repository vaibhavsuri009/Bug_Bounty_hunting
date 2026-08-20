# API: HTTP Method Authorization Bypass

- **What it is:** Access control differs across alternate methods/routes that perform the same action.
- **Where to look:** Endpoints supporting GET, POST, PUT, PATCH, DELETE or duplicate action routes.
- **Source example:** Compare `POST /posts/ID/delete` with `DELETE /posts/ID`.
- **Method:** Capture an authorized action, replay it under lower privilege, and systematically change the HTTP method or equivalent route.
- **Also try:** Removing tokens or adding client-controlled role hints such as `admin=1` only as a validation test.
- **False positives:** Method changes can trigger different functionality; confirm the protected action actually occurs.
- **Remediation:** Centralize authorization so every method and route enforces the same policy.

```http
POST /posts/123/delete
DELETE /posts/123
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 24
