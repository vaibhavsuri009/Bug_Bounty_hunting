# Open Redirect Parameter Hunting

- What it is: User-controlled redirect input sends a browser to an attacker-chosen destination.
- Where to look: Requests containing URL-like parameters such as `url`, `redirect`, `next`, `redirect_to`, `return_to`, `r`, or `u`.
- Capture navigation requests in a proxy and identify parameters that influence a later redirect.
- Replace the suspected destination with a domain you control.
- Example pattern:
```text
https://target.example/?redirect_to=https://attacker.example
```
- Confirm the response or browser ultimately navigates to the supplied external domain.
- Check 3xx responses and the `Location` header rather than relying only on the rendered page.
- Edge case: Parameter names may be non-obvious or only one character long.
- False-positive trap: A redirect restricted to a safe, fixed allowlist is not open.
- Remediation: Resolve and validate redirect destinations against a strict allowlist before redirecting.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 2
