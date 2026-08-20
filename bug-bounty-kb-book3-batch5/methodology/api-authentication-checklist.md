# API Authentication Testing Checklist

- What it is: Authentication testing covers basic login behavior, password reset/MFA, token generation, token handling, and JWTs.
- Where to look / how to identify it:
  - Create a valid baseline first, then test how errors, token expiry, and credential requirements behave.
- Exploitation / test pattern:
  - Use only controlled accounts for brute-force or token tests and obey rate-limit/scope restrictions.
- Tools + exact CLI syntax (if mentioned):
  - Tools mentioned by the book include Burp Intruder, Sequencer, Decoder, Wfuzz, and JWT tooling.
- Common false-positive / WAF / edge-case notes:
  - Do not confuse authorization failures with authentication failures.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use strong MFA, rate limiting, high-entropy tokens, secure JWT validation, and prompt token revocation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. A
