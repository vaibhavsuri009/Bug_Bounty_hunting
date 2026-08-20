# Insecure Deserialization Hunting

- Source review is the most reliable approach: locate deserialization APIs receiving user-controlled data.
- Functions highlighted by the chapter:
```text
PHP:    unserialize()
Java:   readObject()
Python: pickle.loads()
Ruby:   Marshall.load()
```
- Without source, look for large opaque blobs in cookies, parameters, authentication tokens, database inputs, and form data.
- Decode likely base64 data and identify language-specific serialization signatures.
- After identification, tamper with identity/control properties and observe authorization or logic changes.
- Only attempt gadget-chain escalation after confirming the object is actually deserialized.
- False-positive trap: large base64 values may simply be encrypted/signed tokens or ordinary binary data.
- Remediation: use safe data-only formats and never deserialize attacker-controlled native objects without strict constraints.
## Source: Bug Bounty Bootcamp, Ch. 14
