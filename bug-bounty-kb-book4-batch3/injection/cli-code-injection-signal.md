# CLI Code Injection Signal

- What it is: Code injection can occur when API-supplied values are interpreted by a downstream CLI or utility rather than by the operating system directly.
- Where to look / how to identify it:
  - Look for image/video converters, document processors, archive tools, and other commands wrapped by server libraries.
- Exploitation / test pattern:
  - Trace which client fields become CLI options and test only benign unexpected options in a lab.
- Tools + exact CLI syntax (if mentioned):
  - Source review and controlled library invocation.
- Common false-positive / WAF / edge-case notes:
  - Unexpected CLI behavior is not the same as OS command execution.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use structured library APIs, strict option allowlists, and avoid shell/string concatenation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
