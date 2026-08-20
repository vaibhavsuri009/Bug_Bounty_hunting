# Prototype Pollution Property Injection

- What it is: Polluting a shared prototype can cause child objects to inherit attacker-controlled properties they never defined.
- Where to look / how to identify it:
  - Trace authorization/UI decisions that fall back through the prototype chain.
- Exploitation / test pattern:
  - Test with a benign marker such as a nonsecurity property before analyzing sensitive behavior.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Console/source review.
- Common false-positive / WAF / edge-case notes:
  - Own properties can shadow polluted prototype values, reducing impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use own-property checks and prevent prototype mutation from untrusted data.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
