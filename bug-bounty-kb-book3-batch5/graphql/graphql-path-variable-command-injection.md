# GraphQL Path Variable Command Injection

- What it is: A backend path variable can become command injection when it is concatenated into an operating-system command.
- Where to look / how to identify it:
  - Establish a normal mutation response, then test the path variable with a benign separator plus a harmless identity/version command.
- Exploitation / test pattern:
  - Confirm only with non-destructive proof such as the current user or OS version on a lab/authorized target.
- Tools + exact CLI syntax (if mentioned):
  - Example safe validation concept: separator + `whoami` rather than destructive commands.
- Common false-positive / WAF / edge-case notes:
  - GraphQL returning 200 does not mean the command ran; validate the body or a safe side effect.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Never pass GraphQL variables to a shell; use argument-safe process APIs and strict validation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
