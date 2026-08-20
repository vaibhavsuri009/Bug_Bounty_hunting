# Prototype Pollution Recon Signal

- What it is: JavaScript prototypes propagate properties to child objects, so unsafe prototype mutation can influence many objects at runtime.
- Where to look / how to identify it:
  - Identify code that merges attacker-controlled objects, accepts arbitrary keys, or modifies `prototype`/`__proto__` paths.
- Exploitation / test pattern:
  - Record possible prototype mutation points for later dedicated testing.
- Tools + exact CLI syntax (if mentioned):
  - Source review and DevTools runtime inspection.
- Common false-positive / WAF / edge-case notes:
  - Prototype usage itself is normal; the vulnerability requires attacker-controlled modification with security impact.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reject dangerous object keys, use safe merge libraries, null prototypes where appropriate, and freeze critical prototypes.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
