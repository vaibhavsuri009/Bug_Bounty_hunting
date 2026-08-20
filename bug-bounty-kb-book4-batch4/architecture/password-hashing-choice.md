# Password Hashing Algorithm Selection

- What it is: Passwords should be stored with deliberately slow, one-way password hashing rather than plaintext or fast general-purpose hashes.
- Where to look / how to identify it:
  - Review credential storage for plaintext, MD5/SHA-family direct hashing, BCrypt/PBKDF2/Argon2-like schemes, and work factors.
- Exploitation / test pattern:
  - Benchmark the chosen work factor on production-class hardware and ensure verification remains usable.
- Tools + exact CLI syntax (if mentioned):
  - Password-hash library configuration.
- Common false-positive / WAF / edge-case notes:
  - Hashing alone is not sufficient when unsalted or configured with weak work factors.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use a modern password hashing function with salt and tunable cost.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
