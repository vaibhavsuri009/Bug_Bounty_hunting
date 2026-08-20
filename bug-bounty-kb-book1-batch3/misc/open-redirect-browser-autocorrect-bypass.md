# Open Redirect Browser Autocorrect Bypass

- **What it is:** Exploits differences between a URL validator and browser normalization/autocorrection.
- **Where to look:** Redirect filters that block only literal `http://` or `https://` patterns.
- Try malformed separators and slash/backslash variants, then compare validator acceptance with final browser navigation.

```text
https:attacker.example
https;attacker.example
https:\/\/attacker.example
https:\attacker.example
```

- A useful edge case is a backslash near user-info/hostname boundaries.
- Test in multiple browsers because normalization behavior can differ.
- **False positives / edge cases:** A payload that looks accepted but stays on the trusted hostname is not exploitable.
- **Remediation:** Parse and canonicalize URLs with a standards-compliant library before validating the final origin.

## Source: Bug Bounty Bootcamp, Ch. 7
