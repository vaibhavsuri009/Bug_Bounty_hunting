# Rails Signed-Cookie Deserialization RCE

- What it is: A leaked Rails signing secret can allow a crafted serialized cookie to pass integrity checks and reach unsafe deserialization.
- Prerequisites: valid `secret_key_base`, vulnerable Rails version/configuration, and cookie-based session deserialization.
- The book notes Rapid7's Metasploit `Rails Secret Deserialization` exploit for affected legacy Rails.
- Use only in an explicitly authorized environment and prefer a benign `id` proof.
- Confirm the cookie is actually deserialized by the target application.
- False positive: knowing the signing secret alone does not prove exploitable deserialization.
- Edge case: serializer format/version and Rails patches are decisive.
- Remediation: rotate secrets, patch Rails, invalidate sessions, and avoid unsafe object deserialization.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
