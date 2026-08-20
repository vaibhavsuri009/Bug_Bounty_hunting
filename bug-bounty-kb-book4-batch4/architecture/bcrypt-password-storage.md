# BCrypt Password Storage

- What it is: BCrypt is designed to remain expensive to brute-force by using a configurable computational work factor.
- Where to look / how to identify it:
  - Check whether BCrypt is used through a mature library and whether cost settings match current hardware.
- Exploitation / test pattern:
  - Verify new passwords receive fresh salts and the expected work factor.
- Tools + exact CLI syntax (if mentioned):
  - Language-specific BCrypt library.
- Common false-positive / WAF / edge-case notes:
  - Old low-cost settings may no longer provide adequate resistance.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Periodically raise work factor and rehash passwords after successful login.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
