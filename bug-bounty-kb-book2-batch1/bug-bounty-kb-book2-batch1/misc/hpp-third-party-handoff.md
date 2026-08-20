# HPP in Third-Party Service Handoffs

- What it is: Parameters from a target URL can be copied into a downstream service where duplicate-parameter rules change the result.
- Where to look: Social sharing, payment, support, OAuth, analytics, or other features that generate requests to another service.
- Capture the target page and identify parameters copied into the downstream URL.
- Add a duplicate downstream parameter to the source URL, such as a second `u` or `text` value.
- Example pattern:
```text
...?u=https://trusted.example/page&u=https://attacker.example/
```
- Follow the generated handoff and verify which value the downstream service honors.
- Also test parameters not normally present but meaningful to the downstream service.
- False-positive trap: A polluted link with no security-relevant downstream effect is only malformed input.
- Remediation: Reconstruct third-party requests from explicit trusted fields instead of forwarding user-controlled query strings.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 3
