# Open Redirect Validator Logic Bypass

- **What it is:** Bypasses naive checks such as "starts with", "contains", or "ends with" the trusted domain.
- **Where to look:** Redirect parameters that reject obvious external URLs but allow strings containing the target hostname.
- Test hostname-as-subdomain, hostname-in-path, and user-info (`@`) confusion.

```text
https://example.com/login?redir=https://example.com.attacker.example/
https://example.com/login?redir=https://attacker.example/example.com
https://example.com/login?redir=https://example.com@attacker.example/example.com
```

- Always inspect the browser's final parsed hostname, not just the raw string.
- **False positives / edge cases:** Some frameworks normalize and revalidate after parsing, which defeats these tricks.
- **Remediation:** Compare the parsed canonical hostname against an exact allowlist; do not use substring checks.

## Source: Bug Bounty Bootcamp, Ch. 7
