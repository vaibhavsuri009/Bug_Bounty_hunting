# SQLi Inside Base64-Encoded JSON

- What it is: An encoded URL parameter hides structured data that later reaches SQL.
- Look for opaque Base64-like parameters in links, especially email/unsubscribe flows.
- Decode first and inspect for JSON fields such as IDs or email addresses.
```json
{"user_id":"5755","receiver":"user@example.test"}
```
- Inject only into the decoded structure, then re-encode it exactly as the server expects.
- The book's Uber case required Base64 decoding, modification, and re-encoding.
- Compare timing/content before and after the modified request.
- False positive: malformed Base64 or JSON may fail before reaching the database.
- Edge case: URL encoding may be required after Base64 encoding.
- Remediation: treat decoded fields as untrusted and parameterize their database use.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 9
