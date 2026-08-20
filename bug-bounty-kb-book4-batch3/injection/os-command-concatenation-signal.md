# OS Command Concatenation Signal

- What it is: Command injection occurs when client input is concatenated into a shell command executed by the host OS.
- Where to look / how to identify it:
  - Search server code for shell execution functions that embed request parameters or filenames.
- Exploitation / test pattern:
  - Prove only with harmless commands such as identity/version output in a lab or explicitly authorized target.
- Tools + exact CLI syntax (if mentioned):
  - Node.js signal: `child_process.exec()` with string interpolation.
- Common false-positive / WAF / edge-case notes:
  - Execution privileges determine impact; low-privilege processes reduce but do not remove risk.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Avoid shell execution; use argument-safe APIs and strict allowlists.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
