# Android: Review Bundled SQLite/DB Files

- **What it is:** Inspect `.db` and `.sqlite` files shipped with or created by the app for sensitive information.
- **Where to look:** Decompiled APK resources/assets and files pulled from the authorized test device.
- **Data of interest:** Session data, financial information, user data, organizational secrets, or persistent tokens.
- **Method:** Locate database files, inspect tables/records, and determine whether the data should be present or protected.
- **False positives:** Test/demo data may be intentionally non-sensitive; validate whether values are real/current.
- **Edge case:** Encryption may protect the file but keys hardcoded in the APK can undermine it.
- **Remediation:** Minimize local sensitive storage and protect necessary data with platform-backed secure storage.

```bash
find . -type f \( -name '*.db' -o -name '*.sqlite' \)
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
