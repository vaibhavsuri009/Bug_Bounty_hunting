# HPP Signature-Validation / Action Split

- What it is: One duplicate parameter may be used to validate a signature while another is used to perform the action.
- Where to look: Signed links containing IDs plus a signature, HMAC, token, or checksum.
- Begin with a legitimate signed request and identify the parameter bound to the signature.
- Changing the signed ID alone should fail if integrity checking works.
- Add a second copy of the same ID with another value instead of replacing the original.
- Example structure:
```text
...?uid=ATTACKER_ORIGINAL&uid=VICTIM&sig=VALID_FOR_ORIGINAL
```
- Check whether validation accepts the original value while business logic acts on the second value.
- Try reversing duplicate order to identify parser differences.
- False-positive trap: A request is safe if the exact canonical value validated is also the only value used for the action.
- Remediation: Canonicalize parameters before signature verification and use that same canonical representation afterward.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 3
