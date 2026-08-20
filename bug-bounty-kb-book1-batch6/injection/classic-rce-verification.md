# Classic RCE Verification

- **What it is:** Command/code execution results are returned directly in the application response.
- **Where to look:** Suspected code/command injection points where output may be reflected in HTTP responses.
- **Test / exploitation:**
  - Establish a normal-response baseline.
  - Execute a harmless identity or directory-list command.
  - Verify that the exact command result appears in the server response.
  - Use a unique harmless marker if output is ambiguous.
  - Stop after minimal proof; avoid accessing confidential files.
- **Tools / syntax:**
```text
whoami
ls
```
- **False positives / edge cases:**
  - Do not treat an echoed command string as execution; require actual command output.
- **Remediation:** Remove unsafe evaluation/system calls and run the application with least privilege.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
