# Open Redirect Unicode Normalization Bypass

- **What it is:** Uses non-ASCII or look-alike characters to create parser differences between validation and navigation.
- **Where to look:** Redirect validators that accept Unicode before browser normalization.
- Insert non-ASCII characters near hostname/path delimiters and observe the final normalized URL.
- Unicode slash-like or hostname look-alike characters are especially relevant.

```text
https://attacker.example%E2%95%B1.example.com
```

- Test across browsers because normalization and IDN handling differ.
- Focus on whether the final hostname becomes attacker-controlled after normalization.
- **False positives / edge cases:** A visually confusing URL is not enough; the browser must actually navigate to the external host.
- **Remediation:** Normalize Unicode/IDN input before exact origin validation and reject ambiguous encodings.

## Source: Bug Bounty Bootcamp, Ch. 7
