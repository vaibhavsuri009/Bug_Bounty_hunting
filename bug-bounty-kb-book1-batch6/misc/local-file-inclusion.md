# Local File Inclusion (LFI) via Uploaded File

- **What it is:** A local include path is user-controlled, allowing traversal to an uploaded file that the application then executes/includes.
- **Where to look:** Page/language/template include parameters combined with file-upload functionality.
- **Test / exploitation:**
  - Determine the server-side directory used for normal includes.
  - Upload a harmless file to a location whose path you can infer.
  - Use ../ traversal in the include parameter to reach the uploaded file.
  - Confirm the server includes/evaluates the local file.
  - Try encoded traversal only when plain ../ is filtered.
- **Tools / syntax:**
```text
http://example.com/?page=../uploads/malicious.php
http://example.com/?page=..%2fuploads%2fmalicious.php
```
- **False positives / edge cases:**
  - Reading a file is path traversal/LFI; code execution requires the included content to be interpreted by the runtime.
- **Remediation:** Allowlist include targets and isolate user uploads from executable application directories.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
