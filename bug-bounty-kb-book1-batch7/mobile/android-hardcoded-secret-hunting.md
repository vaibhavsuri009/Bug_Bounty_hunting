# Android: Hunt Hardcoded Secrets in APK Resources

- **What it is:** Search decompiled APK resources/source for API keys, secrets, endpoints, and encryption material.
- **Primary location:** `res/values/strings.xml` often contains literal strings needed by the app.
- **Also search:** Decompiled source and other resource files with secret-oriented keywords.
- **Method:** Decompile APK, grep likely keywords, then validate whether discovered credentials are current and privileged.
- **False positives:** Public API identifiers and revoked keys may look sensitive but have no exploitable impact.
- **Edge case:** Obfuscation can hide obvious strings; runtime instrumentation may reveal values.
- **Remediation:** Keep secrets server-side and rotate any credentials shipped in client packages.

```bash
grep -RniE 'key|secret|password|token|api[_-]?key|endpoint' .
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
