# CSRF Double-Submit Cookie Bypass

- **What it is:** Targets defenses that only compare a CSRF cookie value with the request parameter value.
- **Where to look:** Requests where the same token appears in both a cookie and body/query parameter.
- First confirm the server checks equality rather than server-side token validity.
- If an authorized test lets you control the CSRF cookie, set the same arbitrary value in both locations.

```text
Cookie: session=<TEST_SESSION>; csrf_token=test123
csrf_token=test123
```

- A practical exploit additionally requires a legitimate way to influence the victim's CSRF cookie; do not assume this capability.
- **False positives / edge cases:** If the token is cryptographically signed or server-stored, arbitrary equal values will fail.
- **Remediation:** Bind the token to server-side session state or use a signed double-submit design.

## Source: Bug Bounty Bootcamp, Ch. 9
