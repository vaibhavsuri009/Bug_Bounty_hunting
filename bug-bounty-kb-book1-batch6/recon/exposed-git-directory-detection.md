# Exposed .git Directory Detection

- **What it is:** A production server exposes Git metadata that can reveal source code, commit history, and secrets.
- **Where to look:** Application roots and common deployment paths.
- **Test / exploitation:**
  - Request /.git at the application root.
  - Interpret 404 as likely absent; a directory listing means direct exposure.
  - If the root gives 403, request known files such as /.git/config and /.git/HEAD.
  - If known files are readable, proceed to reconstruct only the in-scope repository.
  - Review recovered content for source and secrets.
- **Tools / syntax:**
```text
curl https://example.com/.git/config
curl https://example.com/.git/HEAD
```
- **False positives / edge cases:**
  - 403 on /.git does not prove contents are inaccessible; test known files directly.
- **Remediation:** Block public access to VCS metadata and exclude .git from production deployments.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
