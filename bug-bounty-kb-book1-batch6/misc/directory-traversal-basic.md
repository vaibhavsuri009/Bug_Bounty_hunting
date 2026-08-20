# Directory Traversal via Filepath Input

- **What it is:** User-controlled file paths can escape an intended directory by using parent-directory sequences.
- **Where to look:** Download, image, template, language, attachment, export, or file-view parameters that contain filenames or relative paths.
- **Test / exploitation:**
  - Identify parameters that reference a local file.
  - Replace the expected filename with ../ sequences followed by a known nonsensitive system path.
  - Increase the number of ../ segments until the path reaches the filesystem root.
  - Compare status codes, response size, and returned file content.
  - Stop after proving access; avoid retrieving sensitive data unnecessarily.
- **Tools / syntax:**
```text
../../../../../etc/passwd
```
- **False positives / edge cases:**
  - A generic error after ../ is not proof; verify that an unintended file is actually read.
- **Remediation:** Resolve paths canonically, enforce a fixed base directory, and allowlist permitted files.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 17
