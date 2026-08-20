# Cross-Team Security Review

- What it is: Security-sensitive changes benefit from review by engineers outside the committer's immediate team to reduce blind spots and conflicts of interest.
- Where to look / how to identify it:
  - Identify commits involving auth, crypto, payments, parsers, serialization, permissions, or sensitive data.
- Exploitation / test pattern:
  - Require an independent reviewer before merge/release.
- Tools + exact CLI syntax (if mentioned):
  - GitHub/GitLab branch protection and CODEOWNERS.
- Common false-positive / WAF / edge-case notes:
  - Independent review can still fail without security expertise.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use mandatory reviewers, security ownership rules, and protected branches.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 20
