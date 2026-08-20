# PHP Code-Execution Filter Bypass

- **What it is:** PHP syntax variations reconstruct blocked function names without placing the literal blocked string in the request.
- **Where to look:** Confirmed PHP code injection where filters reject names such as system.
- **Test / exploitation:**
  - Confirm PHP expression/code execution first.
  - Split a blocked function name using PHP string concatenation.
  - Try comments between a function name and invocation where accepted.
  - Try hex-escaped function-name strings.
  - Verify only with harmless commands such as ls.
- **Tools / syntax:**
```text
('sys'.'tem')('ls');
system/**/('ls');
'\x73\x79\x73\x74\x65\x6d'('ls');
```
- **False positives / edge cases:**
  - Some PHP versions/configurations handle callable strings differently; test the exact target behavior.
- **Remediation:** Do not evaluate user-controlled PHP; reject untrusted code paths at the design level.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
