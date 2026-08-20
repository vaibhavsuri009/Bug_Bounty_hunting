# Exact Dependency Version Pinning

- What it is: Exact version pinning prevents normal package-manager semver behavior from silently moving to newer patch releases.
- Where to look / how to identify it:
  - Inspect manifests for caret/tilde ranges on high-risk audited dependencies.
- Exploitation / test pattern:
  - Pin audited versions while maintaining a controlled update process.
- Tools + exact CLI syntax (if mentioned):
  - npm manifest; remove `^` when exact version is intended.
- Common false-positive / WAF / edge-case notes:
  - Pinning can leave known vulnerabilities unfixed if updates are neglected.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Pair exact pins with automated advisory monitoring and deliberate upgrades.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
