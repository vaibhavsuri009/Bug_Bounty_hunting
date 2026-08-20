# Open Redirect Parameter Discovery

- **What it is:** Finds URL-controlled redirect destinations that may be attacker-modifiable.
- **Where to look:** Login, logout, registration, SSO, error, and post-action flows that return users elsewhere.
- Capture traffic in Burp/ZAP and inspect parameters containing absolute or relative URLs.
- Common names: `redirect`, `redir`, `next`, `return`, `returnurl`, `RelayState`, `forward`, `url`, `uri`, `dest`, `destination`.
- Also flag pages returning `301`/`302` without a visible redirect parameter; they may use `Referer`.
- Test only in authorized scope.

```text
/login?redirect=https://example.com/dashboard
/login?next=/dashboard
/logout?dest=/
```

- **False positives / edge cases:** A redirect parameter is not vulnerable if destinations are strictly restricted to trusted origins.
- **Remediation:** Resolve redirects against a strict allowlist of approved origins or use server-side route identifiers.

## Source: Bug Bounty Bootcamp, Ch. 7
