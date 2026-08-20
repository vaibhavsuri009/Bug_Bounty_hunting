# Null-Prototype Objects

- What it is: Objects created without prototypes cannot inherit polluted properties from the normal JavaScript prototype chain.
- Where to look / how to identify it:
  - Use for dictionaries/maps populated with attacker-controlled keys where prototype behavior is unnecessary.
- Exploitation / test pattern:
  - Create with `Object.create(null)` and test expected operations.
- Tools + exact CLI syntax (if mentioned):
  - `const obj = Object.create(null);`
- Common false-positive / WAF / edge-case notes:
  - Null-prototype objects lack inherited helper methods and may require code changes.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use null-prototype maps for untrusted-key containers.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
