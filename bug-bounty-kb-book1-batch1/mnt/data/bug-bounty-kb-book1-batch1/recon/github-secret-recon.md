# GitHub Secret and Source Recon

- What it is: Search public repositories, commits, and issues for secrets, endpoints, vulnerable code, and infrastructure clues.
- Find organization/product GitHub accounts and relevant employee/contributor accounts.
- Enumerate project repositories and top contributors.
- Review **Issues** and **Commits** for unresolved bugs, recent fixes, and security changes.
- Review file **History** and **Blame** to understand how sensitive code evolved.
- Search code for `key`, `secret`, `password`, and similar credential indicators.
- Look for authentication, password reset, state-changing actions, private-data reads, file uploads, and user-input handling.
- Record configuration files, old endpoints, S3 URLs, dependencies, and imported package versions.
- Tools mentioned: Gitrob for sensitive files; TruffleHog for regex/high-entropy secret detection.
- KeyHacks is mentioned for checking how discovered credential types can be validated/used.
- False-positive trap: example/test credentials and revoked keys can look real; validate non-destructively and within scope.
- Remediation: remove/revoke exposed secrets, rotate credentials, and prevent secrets from entering public version control.

## Source: Bug Bounty Bootcamp, Ch. 5
