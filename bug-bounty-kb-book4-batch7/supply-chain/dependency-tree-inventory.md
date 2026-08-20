# Full Dependency Tree Inventory

- What it is: Direct dependencies can pull in fourth-party and deeper dependencies that also affect security.
- Where to look / how to identify it:
  - Generate the complete dependency tree and track every unique package/version.
- Exploitation / test pattern:
  - Evaluate transitive packages rather than only top-level dependencies.
- Tools + exact CLI syntax (if mentioned):
  - `npm ls` / `npm list --depth=<n>`
- Common false-positive / WAF / edge-case notes:
  - Large dependency trees are normal but increase maintenance burden and attack surface.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain automated SBOM/dependency-tree visibility.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
