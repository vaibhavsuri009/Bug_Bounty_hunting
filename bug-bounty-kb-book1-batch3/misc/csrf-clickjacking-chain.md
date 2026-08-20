# CSRF via Clickjacking Chain

- **What it is:** Uses clickjacking to trigger a state-changing action when direct CSRF is blocked by a token.
- **Where to look:** Token-protected actions located on pages that remain frameable cross-origin.
- Frame the legitimate page instead of forging the request directly.
- If the victim can be tricked into clicking the real control inside the frame, the request originates from the legitimate page and includes its valid token.

```html
<iframe src="https://example.com/account/action" width="500" height="500"></iframe>
```

- Validate only with your own test account.
- **False positives / edge cases:** CSP `frame-ancestors`, X-Frame-Options, and SameSite behavior can prevent exploitation.
- **Remediation:** Protect sensitive pages against framing in addition to using CSRF tokens.

## Source: Bug Bounty Bootcamp, Ch. 9
