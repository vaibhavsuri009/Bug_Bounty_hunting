# Code Review: Weak Cryptography Search

- **What it is:** Static review for weak encryption/hashing primitives and weak key handling.
- **Where to look:** Crypto helpers, password hashing, token generation, encryption utilities, and variables storing algorithm names/keys.
- **Search targets mentioned:** `ECB`, `MD4`, and `MD5`, plus similarly named functions/variables such as `md5_hash` or `ecb_key`.
- **Method:** Grep algorithm names, inspect what data they protect, then judge impact based on sensitivity.
- **False positives:** Weak hashing on non-security-sensitive data may have little security impact.
- **Edge case:** A strong algorithm can still be weakly implemented or used with poor keys.
- **Remediation:** Replace weak primitives with current, appropriate cryptographic constructions and key management.

```bash
grep -RniE '\bECB\b|\bMD4\b|\bMD5\b|md5_|ecb_' .
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
