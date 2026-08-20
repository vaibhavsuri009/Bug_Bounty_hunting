# Package Maintainer Account Compromise Risk

- What it is: A compromised package maintainer account can publish malicious releases that downstream applications automatically consume.
- Where to look / how to identify it:
  - Review package ownership changes, maintainer security practices, sudden releases, and unusual dependency updates.
- Exploitation / test pattern:
  - Treat unexpected high-impact package updates as supply-chain incidents rather than ordinary version bumps.
- Tools + exact CLI syntax (if mentioned):
  - Registry history, repository commits, release metadata.
- Common false-positive / WAF / edge-case notes:
  - A new maintainer or release is not proof of compromise.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Require MFA for maintainers, signed provenance, review gates, and restricted update automation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 17
