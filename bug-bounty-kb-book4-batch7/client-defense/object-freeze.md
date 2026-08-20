# Prototype Freezing

- What it is: `Object.freeze()` can prevent runtime modification of sensitive objects and reduce prototype-pollution impact.
- Where to look / how to identify it:
  - Identify security-critical configuration objects that should become immutable after initialization.
- Exploitation / test pattern:
  - Freeze only targeted objects after creation and test legitimate behavior.
- Tools + exact CLI syntax (if mentioned):
  - `Object.freeze(object)`
- Common false-positive / WAF / edge-case notes:
  - Bulk freezing built-ins can break framework/browser functionality.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Freeze narrowly scoped immutable security/configuration objects only.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 34
