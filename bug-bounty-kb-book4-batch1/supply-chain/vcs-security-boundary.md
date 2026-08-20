# Version Control as a Security Boundary

- What it is: Modern web application security depends on source repositories and CI/CD pipelines as well as runtime application code.
- Where to look / how to identify it:
  - Map GitHub/GitLab repositories, deployment hooks, CI/CD systems, package registries, and credential flows when they are in scope.
- Exploitation / test pattern:
  - Treat source-control compromise as a potential route to production deployment.
- Tools + exact CLI syntax (if mentioned):
  - Public records/source review; no special exploit tool required.
- Common false-positive / WAF / edge-case notes:
  - Public repositories can be intentional; look for exposed secrets, sensitive history, or dangerous deployment trust.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use MFA, branch protection, secret scanning, least-privileged CI credentials, and signed/reviewed deployment workflows.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
