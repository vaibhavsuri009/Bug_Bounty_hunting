# Payload Solutions-Space Reduction

- What it is: Brute-force efficiency improves when rules about a field reduce the number of possible values.
- Where to look / how to identify it:
  - Record constraints such as exact length, character set, encoding, type, prefix, suffix, or enum membership.
- Exploitation / test pattern:
  - Use known constraints to generate only plausible candidate values in authorized tests.
- Tools + exact CLI syntax (if mentioned):
  - No fixed tool required; scripting is appropriate.
- Common false-positive / WAF / edge-case notes:
  - Guessing high-entropy secrets remains infeasible even after small reductions.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Generate high-entropy secrets and avoid predictable structure for security tokens.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 5
