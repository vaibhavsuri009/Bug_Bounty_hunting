# OS Command Separator Fuzzing

- What it is: Command injection can occur when API input is concatenated into an operating-system command.
- Where to look / how to identify it:
  - Target query/body/header values tied to system tools; pair separators (`|`, `||`, `&`, `&&`, `;`, quotes) with harmless commands such as `whoami`, `pwd`, `uname -a`, `dir`, `ver`; inspect anomalies.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Echoed command text or parser errors do not prove shell execution.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Avoid shell invocation and pass validated arguments to fixed executables.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
