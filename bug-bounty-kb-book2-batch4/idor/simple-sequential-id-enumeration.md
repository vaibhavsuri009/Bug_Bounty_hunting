# Sequential Numeric IDOR Enumeration

- What it is: Changing a predictable numeric object ID returns another user's protected record.
- Look for integer IDs in URLs, JSON, forms, and POST bodies.
- Add/subtract small values from an object ID you own.
```text
?id=1001
?id=1002
```
- Compare status code, response body, and content length.
- Burp Intruder can automate numeric increment/decrement payloads.
- False positive: `200` may still return a generic "not found/unauthorized" page.
- Edge case: access may differ by HTTP method even for the same endpoint.
- Remediation: authorize every object access against the current authenticated principal.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
