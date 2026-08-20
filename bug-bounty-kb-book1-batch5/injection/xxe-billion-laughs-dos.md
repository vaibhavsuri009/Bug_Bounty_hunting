# XXE Billion-Laughs / XML Bomb

- A billion-laughs payload recursively expands nested XML entities until parser memory/CPU is exhausted.
- The vulnerability exists when entity expansion is enabled without effective resource limits.
- Detection should be based on parser configuration or a safe local/staging reproduction.
- The chapter explicitly warns: **never test this payload against a live target** because it can cause service disruption and financial loss.
- Risk pattern:
```xml
<!ENTITY lol "lol">
<!ENTITY lol1 "&lol;&lol;&lol;&lol;&lol;&lol;&lol;&lol;&lol;&lol;">
<!ENTITY lol2 "&lol1;&lol1;&lol1;&lol1;&lol1;&lol1;&lol1;&lol1;&lol1;&lol1;">
```
- Repeating this nesting exponentially increases expansion size.
- False-positive trap: hardened parsers cap entity expansion depth/count and will reject the document safely.
- Remediation: disable entity expansion where possible and enforce strict parse-depth/time/memory limits.
## Source: Bug Bounty Bootcamp, Ch. 15
