# CSRF Cross-Session Token Bypass

- **What it is:** Tests whether the server accepts any currently valid CSRF token instead of binding it to the victim session.
- **Where to look:** Token-protected actions where token validation may be global rather than session-specific.
- Create two authorized test accounts/sessions.
- Take a valid CSRF token from session A and submit it with session B's state-changing request.

```text
Cookie: session=<SESSION_B>
csrf_token=<TOKEN_FROM_SESSION_A>
```

- If the request succeeds, the token is valid but not correctly bound to the active user/session.
- **False positives / edge cases:** Some anti-CSRF schemes intentionally use a site-wide secret plus additional hidden binding; verify repeatability.
- **Remediation:** Bind tokens to the authenticated session and validate that binding server-side.

## Source: Bug Bounty Bootcamp, Ch. 9
