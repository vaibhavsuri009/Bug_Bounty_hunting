# npm Manifest Detection

- What it is: `package.json` and lockfiles reveal JavaScript package-manager usage and exact or constrained dependency versions.
- Where to look / how to identify it:
  - Look for `package.json`, `package-lock.json`, yarn/pnpm lockfiles, and build scripts.
- Exploitation / test pattern:
  - Use the manifest to map direct dependencies and the lockfile to identify resolved versions.
- Tools + exact CLI syntax (if mentioned):
  - `npm ls --all` on an authorized/local codebase.
- Common false-positive / WAF / edge-case notes:
  - Public manifests may intentionally expose dependency names.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep lockfiles committed, scan dependencies, and enforce trusted registries.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
