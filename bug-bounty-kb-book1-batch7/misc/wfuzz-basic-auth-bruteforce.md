# Wfuzz: Basic Authentication Fuzzing

- **What it is:** Test HTTP Basic Authentication credentials using controlled username/password wordlists.
- **Where to look:** Authorized endpoints returning 401/403 and using `Authorization: Basic ...`.
- **Header method:** Fuzz a prebuilt Base64 credential list in the Authorization header.
- **Built-in method:** Use two wordlists with `FUZZ` and `FUZ2Z` plus `--basic`.
- **Validation:** Look for a response pattern that differs from invalid credentials and manually confirm.
- **Safety:** Brute-force only when explicitly permitted; respect lockout/rate-limit policies.
- **Remediation:** Enforce strong credentials, MFA where appropriate, lockouts/rate limits, and monitoring.

```bash
wfuzz -w wordlist.txt -H "Authorization: Basic FUZZ" http://example.com/admin
wfuzz -w usernames.txt -w passwords.txt --basic FUZZ:FUZ2Z http://example.com/admin
```

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 25
