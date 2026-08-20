# URI-Decoding Render Test

- What it is: Encoded input may bypass an earlier filter and be decoded only when rendered.
- Look for inputs that accept percent-encoded characters in parameters or form values.
- Compare a literal character with its URI-encoded equivalent.
```text
/    -> %2F
<    -> %3C
>    -> %3E
```
- Observe the final HTML and page source, not only the submitted request.
- A useful signal is an encoded value becoming a structural HTML character downstream.
- Repeat across all locations where the same value is displayed.
- Tools: CyberChef can produce and decode URI/HTML encodings.
- False positive: decoding alone is normal; it matters only if the decoded value reaches an unsafe rendering context.
- Edge case: multiple decode passes can change behavior, so compare single and nested encoding cautiously.
- Remediation: normalize input once and apply context-aware output encoding at every sink.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 5
