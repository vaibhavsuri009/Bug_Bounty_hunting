# Local `git diff` Security Review Workflow

- What it is: A local branch comparison gives reviewers the complete changed-file list and exact code modifications.
- Where to look / how to identify it:
  - Update main, check out the feature branch, and compare it against origin/main.
- Exploitation / test pattern:
  - Use the diff as the entry point, then trace affected security boundaries and dependencies.
- Tools + exact CLI syntax (if mentioned):
  - `git checkout main`; `git pull origin main`; `git checkout <branch>`; `git diff origin/main...`
- Common false-positive / WAF / edge-case notes:
  - Diff-only review can miss security assumptions in unchanged surrounding code.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Review changed code in full context and test the integrated feature.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
