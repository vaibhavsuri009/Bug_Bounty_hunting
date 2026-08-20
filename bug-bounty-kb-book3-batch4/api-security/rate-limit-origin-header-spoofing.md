# Rate-Limit Origin-Header Spoofing Test

- What it is: A rate limiter may incorrectly trust client-supplied IP/origin headers.
- Where to look / how to identify it:
  - Using a controlled account, vary headers such as `X-Forwarded-For`, `X-Originating-IP`, `X-Remote-IP`, `X-Client-IP`, `X-Remote-Addr`; verify whether rate-limit counters reset.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Trusted reverse proxies may overwrite these correctly, making client values irrelevant.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Strip untrusted forwarding headers and derive client identity only from trusted proxies.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
