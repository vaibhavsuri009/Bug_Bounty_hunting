# Password Entropy Policy

- What it is: Secure password policy should reduce predictable/common patterns rather than relying only on arbitrary complexity rules.
- Where to look / how to identify it:
  - Reject known common passwords and obvious user-specific values such as names or birthdates.
- Exploitation / test pattern:
  - Validate policy with representative weak and strong passwords in test environments.
- Tools + exact CLI syntax (if mentioned):
  - Common-password blocklist and password-strength tooling.
- Common false-positive / WAF / edge-case notes:
  - Overly rigid complexity rules can cause predictable substitutions and user frustration.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer long passwords/passphrases, common-password blocking, and MFA.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
