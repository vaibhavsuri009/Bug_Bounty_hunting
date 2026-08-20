# HTTP Parameter Pollution: Duplicate Parameter Precedence

- What it is: Sending the same parameter multiple times can make different components use different values.
- Where to look: Security-sensitive parameters such as IDs, account numbers, actions, amounts, redirect targets, or signed values.
- Start from a normal request containing one parameter.
- Add a duplicate parameter with a different value:
```text
?from=12345&to=67890&amount=5000&from=ABCDEF
```
- Compare validation, response, and resulting action to determine which occurrence wins.
- Repeat with the attacker value first and last.
- The book notes handling differs by server technology; do not assume a universal first/last rule.
- False-positive trap: Duplicate values that are consistently rejected or normalized are not exploitable HPP.
- Remediation: Reject duplicate security-sensitive parameters or canonicalize once before validation and use.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 3
