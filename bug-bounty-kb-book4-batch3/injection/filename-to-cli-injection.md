# Filename-to-CLI Injection Signal

- What it is: Even a seemingly harmless filename can become an injection vector if it is later inserted into a command-line string.
- Where to look / how to identify it:
  - Trace uploaded filenames through conversion, deletion, compression, or shell-helper operations.
- Exploitation / test pattern:
  - Use controlled filenames containing benign separators to determine whether the string is interpreted structurally.
- Tools + exact CLI syntax (if mentioned):
  - Source review is preferred; avoid destructive command strings.
- Common false-positive / WAF / edge-case notes:
  - Some libraries safely escape filenames; confirm actual interpreter boundaries.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Treat filenames as untrusted and pass them as argument arrays, not shell strings.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 13
