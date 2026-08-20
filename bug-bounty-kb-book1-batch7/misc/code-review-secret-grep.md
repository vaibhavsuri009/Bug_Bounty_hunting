# Code Review: Hardcoded Secret Hunting

- **What it is:** Search source for embedded API keys, tokens, passwords, encryption keys, and other credentials.
- **Where to look:** Source, scripts, config references, JavaScript bundles, test code, and commit history.
- **Keywords:** `key`, `secret`, `password`, `encrypt`, `API`, `login`, `token`.
- **Pattern method:** Add format-specific regexes; the book gives `[a-f0-9]{40}` as an example of a 40-character hex token search.
- **Entropy method:** High-entropy strings can reveal secrets that lack a known prefix/format; TruffleHog is cited for regex + entropy scanning.
- **False positives:** Random IDs and hashes may resemble credentials; validate that a discovered secret is actually used.
- **Remediation:** Remove hardcoded secrets, rotate exposed credentials, and use a secret-storage system.

```bash
grep -RniE 'key|secret|password|encrypt|api|login|token' .
grep -RnoE '[a-f0-9]{40}' .
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 22
