# Low-Privilege Admin Action Test

- What it is: BFLA exists when a low-privileged account can perform an administrative function.
- Where to look / how to identify it:
  - Find admin actions from docs, collections or reverse engineering; replay the exact request with a low-privileged token and verify sensitive data/action changes.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A successful-looking response may not perform the privileged action.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce function-level authorization for every admin endpoint.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
