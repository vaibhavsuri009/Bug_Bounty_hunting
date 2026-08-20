# Open Redirect Bypass Chaining

- **What it is:** Combines multiple redirect-parser tricks when a single bypass is insufficient.
- **Where to look:** Layered validators that check several weak conditions independently.
- Combine allowlist-substring confusion with encoding or user-info parsing.

```text
https://example.com%252f@attacker.example/example.com
```

- Check each stage separately: decoding, canonicalization, validation, then browser navigation.
- Record which control each component bypasses so the report demonstrates root cause.
- **False positives / edge cases:** Complex strings may be rewritten by proxies, frameworks, or browsers before reaching the vulnerable handler.
- **Remediation:** Canonicalize first, parse once, then validate exact scheme/host/port against an allowlist.

## Source: Bug Bounty Bootcamp, Ch. 7
