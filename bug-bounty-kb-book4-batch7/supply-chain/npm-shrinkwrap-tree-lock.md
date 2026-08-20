# npm Shrinkwrap Full Tree Lock

- What it is: `npm shrinkwrap` records exact versions across the dependency tree, not only top-level packages.
- Where to look / how to identify it:
  - Use where reproducible, reviewed dependency trees are a security requirement.
- Exploitation / test pattern:
  - Generate and review `npm-shrinkwrap.json` before release.
- Tools + exact CLI syntax (if mentioned):
  - `npm shrinkwrap`
- Common false-positive / WAF / edge-case notes:
  - A registry maintainer reusing the same version number can still undermine version-only integrity.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Combine tree locking with integrity hashes, Git SHAs, or trusted mirrors.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
