# Security Review at Merge

- What it is: Merge/pull requests are a practical point for security review because the feature is integrated enough to assess as a whole.
- Where to look / how to identify it:
  - Identify security-sensitive merge requests and require security-aware reviewers before merging.
- Exploitation / test pattern:
  - Review the complete diff and integrated feature behavior, not isolated commits only.
- Tools + exact CLI syntax (if mentioned):
  - GitHub/GitLab/Bitbucket review workflow.
- Common false-positive / WAF / edge-case notes:
  - Very large merge requests reduce review quality.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep changes reviewable, require owners, and gate high-risk merges on security approval.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
