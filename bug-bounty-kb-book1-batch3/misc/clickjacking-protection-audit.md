# Clickjacking Protection Audit

- **What it is:** Evaluates whether framing defenses actually protect a sensitive action.
- **Where to look:** State-changing pages and authenticated workflows.
- Inspect for these controls in the response and session cookie.

```text
X-Frame-Options: DENY
X-Frame-Options: SAMEORIGIN
Content-Security-Policy: frame-ancestors 'none';
Content-Security-Policy: frame-ancestors 'self';
Set-Cookie: session=...; SameSite=Strict
```

- If neither framing headers nor effective SameSite behavior exist, perform a frameability test.
- Treat obsolete/unsupported directives as weak protection.
- **False positives / edge cases:** JavaScript frame-busting may block basic tests but can be unreliable.
- **Remediation:** Prefer CSP `frame-ancestors`; use `X-Frame-Options` as defense-in-depth and SameSite cookies for authenticated actions.

## Source: Bug Bounty Bootcamp, Ch. 8
