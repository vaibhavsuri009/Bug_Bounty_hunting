# Custom Cryptography Risk Signal

- What it is: Reinventing cryptography, databases, isolation, or memory-management primitives is a high-risk architectural signal.
- Where to look / how to identify it:
  - Search architecture/code for proprietary cryptographic algorithms, homegrown hashing, or replacement implementations of mature security primitives.
- Exploitation / test pattern:
  - Prioritize custom security primitives for expert review rather than treating uniqueness as a security benefit.
- Tools + exact CLI syntax (if mentioned):
  - Source/design review.
- Common false-positive / WAF / edge-case notes:
  - Custom implementation is not automatically vulnerable, but it lacks the scrutiny of mature standards.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use established, reviewed cryptographic libraries and standard algorithms.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 7
