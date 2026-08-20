# Multiple Versions of Same Dependency

- What it is: One application can transitively load several versions of the same dependency, leaving old vulnerable copies even when the direct version is patched.
- Where to look / how to identify it:
  - Search dependency trees for duplicate package names with different versions.
- Exploitation / test pattern:
  - Evaluate every unique version against security advisories.
- Tools + exact CLI syntax (if mentioned):
  - Package-manager dependency tree tools.
- Common false-positive / WAF / edge-case notes:
  - Deduplication may be impossible if parent packages require incompatible versions.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Upgrade parent dependencies and minimize legacy duplicate versions.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
