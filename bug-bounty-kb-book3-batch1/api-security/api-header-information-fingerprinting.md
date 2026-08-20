# API Header Information Fingerprinting

- What it is: Request/response headers can reveal authentication type, backend technology, timing, and rate-limit state.
- Inspect `Authorization`, `Content-Type`, and middleware `X-*` headers.
- Useful examples include `X-Powered-By`, `X-Response-Time`, `X-API-Key`, and rate-limit headers.
- Record version strings and backend product names for later vulnerability research.
- Track `X-RateLimit-Remaining` or similar values while testing limits.
- Compare timing headers for existing vs nonexistent resources.
- False positive: headers can be inserted or rewritten by proxies and may not represent the origin server.
- Edge case: security headers can reveal configuration but are not vulnerabilities by themselves.
- Remediation: remove unnecessary technology/version disclosure and normalize error/timing behavior.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 2
