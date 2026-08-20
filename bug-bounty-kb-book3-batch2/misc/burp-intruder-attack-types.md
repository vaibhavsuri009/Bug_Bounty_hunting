# Burp Intruder Attack Types

- What it is: Intruder attack types control how multiple payload sets map to attack positions.
- `Sniper`: one payload set; replaces one marked position at a time.
- `Battering ram`: one payload is inserted into all marked positions simultaneously.
- `Pitchfork`: multiple payload sets advance in parallel, preserving pairings.
- `Cluster bomb`: tries every combination across multiple payload sets.
- Use Sniper for a single fuzz point and Battering Ram for the same probe across several fields.
- Use Pitchfork for known username:password pairs.
- Use Cluster Bomb when combinations must be explored and scope/rate limits permit it.
- False positive: a successful response can still be an application-level denial.
- Remediation: rate-limit and authenticate sensitive functions; do not depend on request-shape assumptions.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 4
