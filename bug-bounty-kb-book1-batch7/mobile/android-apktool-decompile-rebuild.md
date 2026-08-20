# Android: Apktool Decompile and Rebuild

- **What it is:** Decode an APK into inspectable files and rebuild it after controlled modifications.
- **Where useful:** Manifest/resource inspection, source/resource modification, and testing behavioral changes.
- **Decode command:** `apktool d example.apk`.
- **Rebuild command:** `apktool b example -o example.apk`.
- **Workflow:** Decode → inspect/modify → rebuild → install on test device/emulator → validate.
- **Edge case:** A rebuilt APK may need proper signing before installation depending on the environment.
- **Remediation:** Do not rely on client APK secrecy for security decisions; enforce controls server-side.

```bash
apktool d example.apk
apktool b example -o example.apk
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 23
