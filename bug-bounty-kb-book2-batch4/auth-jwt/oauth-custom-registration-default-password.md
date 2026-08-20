# OAuth Custom Registration Default-Password Flaw

- What it is: A custom OAuth signup step creates a local account using a predictable placeholder password.
- Monitor the complete OAuth flow, especially nonstandard POST requests after token exchange.
- Look for fields such as:
```json
{"password":"not-provided"}
```
- Log out and test the placeholder password only against your own OAuth-created account.
- The Flurry example allowed normal password login using the literal default value.
- False positive: a placeholder may be ignored by the authentication backend.
- Edge case: only accounts created through one identity provider may be affected.
- Remediation: do not create usable password credentials for federated-only accounts.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 17
