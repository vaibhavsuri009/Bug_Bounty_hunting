# API Rate-Limit Identification

- What it is: Rate limiting can be identified through documentation, headers and behavior after controlled request bursts.
- Where to look / how to identify it:
  - Check `x-rate-limit`, `x-rate-limit-remaining`, `Retry-After`, and `429 Too Many Requests`; determine whether limits are keyed by IP, token, account or route.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A high limit is not the same as no limit; test within approved thresholds.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use centralized quotas keyed to user/token/IP and sensitive action.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
