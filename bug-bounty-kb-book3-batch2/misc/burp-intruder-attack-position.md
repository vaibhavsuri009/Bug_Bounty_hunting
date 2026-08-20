# Burp Intruder Attack-Position Fuzzing

- What it is: Intruder replaces selected request positions with payloads and sends a request series.
- Capture a request and send it to Intruder.
- Clear automatic positions, then wrap the exact field to fuzz with `§...§`.
- Load a payload set: words, numbers, symbols, IDs, usernames, etc.
- Start the attack and sort responses by status, length, or other anomalies.
- Use numeric payload ranges for resource-ID enumeration.
- False positive: response variation alone does not prove a vulnerability.
- Edge case: Community Edition is intentionally slower than Pro.
- Remediation: enforce authorization, validation, and throttling independently of input shape.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
