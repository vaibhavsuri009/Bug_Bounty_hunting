# CSRF Referer-Header Bypass

- **What it is:** Bypasses weak CSRF defenses that trust the `Referer` header.
- **Where to look:** Tokenless endpoints that reject cross-site requests based on referrer checks.
- First test whether omitting the header bypasses validation.

```html
<meta name="referrer" content="no-referrer">
```

- If substring matching is used, test whether the target hostname can appear as an attacker-controlled subdomain or path.

```text
Referer: https://example.com.attacker.example/
Referer: https://attacker.example/example.com
```

- **False positives / edge cases:** Strict origin parsing will reject these forms; browser referrer policy also affects what is sent.
- **Remediation:** Use anti-CSRF tokens and strict `Origin` validation; never rely on substring checks of `Referer`.

## Source: Bug Bounty Bootcamp, Ch. 9
