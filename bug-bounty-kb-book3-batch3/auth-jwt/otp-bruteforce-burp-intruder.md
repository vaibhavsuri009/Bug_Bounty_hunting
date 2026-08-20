# OTP Brute Force with Burp Intruder

- What it is: Short OTPs become guessable when verification lacks effective attempt limits.
- Where to look / how to identify it:
  - Capture your own OTP request; mark OTP; Intruder → Brute forcer; for 4 numeric digits use charset `0123456789`, min/max `4`; compare success to invalid baseline.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - OTP expiry/attempt limits may block testing.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Strict limits, short expiry, replay prevention and account/session binding.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
