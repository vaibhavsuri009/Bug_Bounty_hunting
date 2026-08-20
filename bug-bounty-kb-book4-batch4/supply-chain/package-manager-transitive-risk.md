# Transitive Dependency Risk

- What it is: Package managers automatically resolve child dependencies, expanding the code and trust surface beyond direct dependencies.
- Where to look / how to identify it:
  - Inspect lockfiles and dependency trees rather than only top-level package declarations.
- Exploitation / test pattern:
  - Flag stale, abandoned, vulnerable, or unexpectedly privileged transitive dependencies.
- Tools + exact CLI syntax (if mentioned):
  - `npm ls`, Maven dependency tree, or equivalent package-manager tooling.
- Common false-positive / WAF / edge-case notes:
  - Large dependency trees are common and not inherently vulnerable.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Pin versions, use lockfiles, dependency scanning, and minimize unnecessary packages.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
