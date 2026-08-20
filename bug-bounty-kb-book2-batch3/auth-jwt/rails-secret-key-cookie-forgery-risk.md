# Rails `secret_key_base` Cookie-Forgery Risk

- What it is: Exposing Rails `secret_key_base` can undermine signed-cookie integrity.
- Look for the secret in public repositories, environment examples, backups, or deployment files.
- Rails signs serialized cookie data and verifies the signature on later requests.
- If the signing secret is exposed, an attacker may be able to create modified cookies with valid signatures.
- This becomes especially dangerous in legacy setups that deserialize cookie content unsafely.
- Validate framework/version and cookie store before claiming RCE.
- False positive: a leaked secret may be stale, rotated, or belong to a non-production environment.
- Edge case: modern Rails versions have changed serialization/default protections.
- Remediation: rotate `secret_key_base`, invalidate sessions, and remove secrets from source control.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
