# Recursive Download of Exposed .git

- **What it is:** When directory listing is enabled, the exposed Git metadata can be downloaded recursively for offline reconstruction.
- **Where to look:** A confirmed publicly browsable /.git directory.
- **Test / exploitation:**
  - Verify the directory is in scope and publicly listable.
  - Recursively download the exposed .git directory.
  - Inspect HEAD, refs, logs, objects, and config offline.
  - Use Git tooling to reconstruct source and commit history.
  - Scan only the recovered in-scope repository for secrets.
- **Tools / syntax:**
```text
wget -r example.com/.git
```
- **False positives / edge cases:**
  - Recursive downloads can generate many requests; follow program rate limits.
- **Remediation:** Remove VCS metadata from web roots and deny access at the web server.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 21
