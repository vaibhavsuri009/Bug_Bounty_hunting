# Password Spraying with Intruder Cluster Bomb

- What it is: Try a short likely-password list across many authorized test usernames.
- Where to look / how to identify it:
  - Mark username/password; choose Cluster Bomb; payload 1=usernames, payload 2=short policy-aware passwords; sort by status/length.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Can cause lockouts; successful primary auth may still require MFA.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: MFA, backoff, anomaly detection, breached-password screening.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
