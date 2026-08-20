# GitHub API Secret History Review

- What it is: Current code, commits, issues, and pull requests can expose API keys, tokens, passwords, and endpoint details.
- Search the target name with terms like `api-key`, `password`, `token`, and `secret`.
- In Code, inspect source and use history to review prior versions.
- In commit diffs, look for secrets that were removed from the current code.
- In Issues and Pull Requests, inspect discussions and Files Changed for still-exposed credentials.
- Correlate leaked values with the endpoint or service they belong to.
- False positive: revoked/example keys may no longer work.
- Edge case: never assume a GitHub organization belongs to the target without confirming ownership.
- Remediation: rotate exposed secrets and enable repository secret-scanning controls.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
