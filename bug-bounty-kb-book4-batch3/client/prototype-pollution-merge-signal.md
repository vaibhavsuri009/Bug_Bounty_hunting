# Prototype Pollution via Unsafe Merge

- What it is: Prototype pollution can occur when attacker-controlled object keys are merged into JavaScript prototypes.
- Where to look / how to identify it:
  - Search for recursive merge/update helpers that accept arbitrary keys such as `__proto__` or constructor paths.
- Exploitation / test pattern:
  - Use a local test object and harmless marker property to determine whether prototype state changes.
- Tools + exact CLI syntax (if mentioned):
  - Source review and DevTools Console.
- Common false-positive / WAF / edge-case notes:
  - Property injection into one ordinary object is not prototype pollution unless ancestor state changes.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reject dangerous keys and use safe merge implementations/null-prototype objects.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 16
