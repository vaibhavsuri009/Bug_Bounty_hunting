# Wfuzz Request Throttling

- What it is: Wfuzz can be slowed to stay within a known rate limit during authorized testing.
- Where to look / how to identify it:
  - Use `-t` to limit concurrent connections and `-s` for delay; book examples: `-s 0.01` ≈10 req/s, `-s 1`=1 req/s, `-s 6`≈10/min, `-s 60`=1/min.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Real throughput varies with latency and concurrency.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Enforce meaningful per-account/action limits, not only IP throttles.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
