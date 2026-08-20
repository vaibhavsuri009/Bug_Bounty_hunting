# Burp Sequencer Token Randomness Analysis

- What it is: Sequencer evaluates whether cookies, tokens, keys, or other values contain sufficient entropy.
- Identify a response that generates a fresh token or cookie.
- Send the request/token location to Burp Sequencer.
- Collect a large sample of generated values.
- Review Burp’s entropy/randomness analysis for predictable structure.
- Compare prefixes, suffixes, timestamps, and changing segments manually as well.
- False positive: visible patterns do not prove the unpredictable portion is weak.
- Edge case: server-side state can make an opaque low-entropy-looking token unforgeable.
- Remediation: generate authentication tokens with a cryptographically secure RNG and enough entropy.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
