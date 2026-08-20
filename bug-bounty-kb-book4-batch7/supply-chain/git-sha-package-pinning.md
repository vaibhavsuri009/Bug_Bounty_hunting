# Git SHA Dependency Pinning

- What it is: Referencing an immutable reviewed Git commit provides stronger integrity than trusting mutable package version metadata.
- Where to look / how to identify it:
  - Use for tightly integrated or high-risk dependencies when reproducibility matters.
- Exploitation / test pattern:
  - Pin a reviewed commit and update only through an explicit security review.
- Tools + exact CLI syntax (if mentioned):
  - Git SHA-based package references.
- Common false-positive / WAF / edge-case notes:
  - Repository compromise can still affect future commits; verify provenance.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use immutable revisions plus code review/signing/provenance verification.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 35
