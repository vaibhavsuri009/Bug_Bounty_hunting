# Password Reset / MFA Code Rate-Limit Test

- What it is: Short numeric reset or MFA codes become brute-forceable when verification requests are not rate limited.
- Use only your own account and a code issued to you.
- Send repeated incorrect code attempts and record response behavior.
- A six-digit code has 1,000,000 possibilities; a four-digit code has 10,000.
- Verify lockout, backoff, expiry, attempt counters, and per-account/IP/device limits.
- Stop well before service impact or account lockout unless explicitly authorized.
- False positive: unlimited requests may still be safe if codes expire extremely quickly or other binding controls exist.
- Edge case: rate limits may differ across API versions or reset vs MFA endpoints.
- Remediation: enforce strict attempt limits, short expiry, and account/session binding.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
