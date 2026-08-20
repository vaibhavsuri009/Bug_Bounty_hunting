# WAF/CDN Detection from Headers

- What it is: Response headers and redirects can reveal a WAF/CDN or API gateway in front of the application.
- Where to look / how to identify it:
  - Baseline normal requests; inspect headers such as `X-CDN`, `Server`, `X-Kong-Proxy-Latency`, `X-Original-URI`; watch for 302 redirects to CDN infrastructure.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Headers can be rewritten or spoofed by intermediaries.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Keep edge controls documented and do not rely on obscurity.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
