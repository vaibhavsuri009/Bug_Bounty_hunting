# Malicious Transitive Package Risk

- What it is: An apparently safe dependency can import a malicious subdependency that executes during installation or runtime.
- Where to look / how to identify it:
  - Inspect recently added child dependencies and package install scripts.
- Exploitation / test pattern:
  - Trace how a transitive package entered the dependency graph and what code executes automatically.
- Tools + exact CLI syntax (if mentioned):
  - Package lockfile + dependency graph.
- Common false-positive / WAF / edge-case notes:
  - Many transitive packages are legitimate; focus on unexpected execution privileges and suspicious changes.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use dependency policies, allowlists, sandboxed builds, and automated supply-chain scanning.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
