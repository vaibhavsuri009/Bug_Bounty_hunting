# Rate-Limit Path Variant Test

- What it is: Rate-limit counters may be keyed to raw paths instead of canonical routes.
- Where to look / how to identify it:
  - After hitting a test limit, try semantically equivalent path variants such as `%00`, `%20`, case changes, hyphen variants, or a meaningless query parameter and check whether the counter resets.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - A path variation may hit a different legitimate route rather than bypass the same limiter.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Canonicalize routing before applying rate-limit keys.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
