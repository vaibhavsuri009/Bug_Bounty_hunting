# Git History Secret Recon

- What it is: Git keeps historical commits, so secrets removed from the current file may remain in repository history.
- Where to look / how to identify it:
  - Review authorized/public repositories and relevant historical changes for accidentally committed secrets and endpoints.
- Exploitation / test pattern:
  - Record the commit and affected credential, then validate only whether rotation occurred using safe means.
- Tools + exact CLI syntax (if mentioned):
  - Git history, repository web UI, or local `git log`/`git show`.
- Common false-positive / WAF / edge-case notes:
  - Old credentials may already be revoked; do not assume impact without validation.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Rotate exposed secrets, purge when necessary, enable secret scanning, and prevent commits with pre-commit/CI checks.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
