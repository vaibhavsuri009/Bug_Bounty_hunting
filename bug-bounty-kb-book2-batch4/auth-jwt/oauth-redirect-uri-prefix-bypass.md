# OAuth `redirect_uri` Prefix Validation Bypass

- What it is: The authorization server checks only whether `redirect_uri` starts with an approved string.
- Register/use a controlled OAuth client and inspect its approved callback.
- Append attacker-controlled hostname material to the allowed prefix.
```text
https://www.example.com.attacker.example/
```
- If accepted, complete OAuth only with your own test account and verify where the token/code is delivered.
- Test exact host boundaries, path boundaries, and scheme changes.
- False positive: acceptance during authorization may still be blocked at token exchange.
- Edge case: wildcard callback registrations broaden the attack surface.
- Remediation: exact-match normalized redirect URIs against pre-registered values.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 17
