# Encoded ID Bypass

- **What it is:** An application may hide predictable IDs behind reversible encodings without adding authorization.
- **Where to look:** Long or opaque object identifiers in URLs, JSON, cookies, or API parameters.
- Compare identifiers from two controlled accounts.
- Try common encodings: Base64, Base64URL, URL encoding, HTML encoding, hex, and octal.
- Decode the value and check whether it reveals a simple object ID.
- Replace the decoded ID with the victim test account's ID, then re-encode it.

```text
MTIzNQ -> 1235
MTIzNg -> 1236
```

- **Tools:** Burp Decoder; use Smart Decode when the encoding is unknown.
- **False positives / edge cases:** Encoding or hashing alone is not a vulnerability if strict authorization is still enforced.
- **Remediation:** Treat identifiers as untrusted and enforce object-level access control regardless of representation.

## Source: Bug Bounty Bootcamp, Ch. 10
