# API Token Entropy Analysis

- What it is: Weak token generation may produce predictable authentication tokens.
- Collect a sample of tokens generated for accounts you control.
- Compare length, character set, prefixes/suffixes, timestamps, counters, and repeated segments.
- Generate tokens at different times/accounts to test whether parts correlate with predictable values.
- Do not attempt to hijack real users; use controlled accounts to prove predictability.
- Hardcoded tokens in JavaScript/repositories should be tested separately as exposure issues.
- False positive: visual similarity does not prove practical predictability when a strong random component remains.
- Edge case: encoded tokens may need decoding before structural analysis.
- Remediation: use cryptographically secure random token generation with sufficient entropy.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
