# Shell Command Injection

- **What it is:** User input is concatenated into a shell command, allowing shell metacharacters to append additional commands.
- **Where to look:** Features invoking wget, ping, image/video utilities, converters, diagnostics, or other OS commands using user-controlled values.
- **Test / exploitation:**
  - Identify input that appears to become part of a system command.
  - Inject a shell separator followed by a harmless command.
  - Use output-based verification with ls/whoami when the response includes command output.
  - For blind endpoints, use sleep and compare response timing.
  - Try alternate separators only when the basic form is filtered.
- **Tools / syntax:**
```text
;ls;
| sleep 10;
& sleep 10;
$(sleep 10)
```
- **False positives / edge cases:**
  - Network latency can mimic a sleep-based result; repeat baseline and test requests.
- **Remediation:** Avoid shell invocation; use language APIs and strict argument handling instead of string concatenation.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
