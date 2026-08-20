# Blind Mass Assignment Variable Fuzzing

- What it is: When field names are unknown, candidate privileged property names can be fuzzed into a request.
- Where to look / how to identify it:
  - Test one candidate per request where possible: `admin`, `isadmin`, `role`, `user_priv`, `org`, `credit`, etc.; confirm any accepted property through a secondary controlled read/action.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Many frameworks silently ignore unknown keys.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reject unknown properties and define explicit request schemas.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
