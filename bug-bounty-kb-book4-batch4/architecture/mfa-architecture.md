# MFA Architecture

- What it is: MFA reduces account compromise by requiring a second independent factor in addition to a password.
- Where to look / how to identify it:
  - Map enrollment, recovery, verification, token lifetime, and factor-reset workflows.
- Exploitation / test pattern:
  - Threat-model lost devices, SIM swapping, recovery abuse, backup codes, and administrator resets.
- Tools + exact CLI syntax (if mentioned):
  - Authenticator app/FIDO/WebAuthn/SMS depending design.
- Common false-positive / WAF / edge-case notes:
  - SMS MFA is weaker than phishing-resistant hardware-backed methods but still improves password-only security.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Prefer phishing-resistant MFA and secure recovery/enrollment flows.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
