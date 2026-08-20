# Open Redirect Double-Encoding Bypass

- **What it is:** Exploits mismatched URL-decoding depth between validation code and the browser/framework.
- **Where to look:** Filters that decode once before checking a redirect URL.
- Encode delimiter characters such as `/`, then repeat encoding to test double/triple decode behavior.

```text
https://example.com%2f@attacker.example
https://example.com%252f@attacker.example
https://example.com%25252f@attacker.example
```

- Compare the validator's accepted string with the final browser destination after all decoding/normalization.
- Test both over-decoding and under-decoding assumptions.
- **False positives / edge cases:** Many modern URL libraries canonicalize before validation and will reject these forms.
- **Remediation:** Canonicalize once with a trusted parser, then validate the canonical hostname and scheme.

## Source: Bug Bounty Bootcamp, Ch. 7
