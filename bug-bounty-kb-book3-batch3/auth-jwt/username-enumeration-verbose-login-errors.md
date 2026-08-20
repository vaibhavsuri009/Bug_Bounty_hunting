# Username Enumeration via Verbose Login Errors

- What it is: Authentication errors reveal whether an account exists.
- Where to look / how to identify it:
  - Compare invalid username vs valid controlled username + wrong password; look for `User does not exist` vs `Invalid password` or equivalent.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Localization/backend routing may alter messages.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Return one generic authentication failure.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
