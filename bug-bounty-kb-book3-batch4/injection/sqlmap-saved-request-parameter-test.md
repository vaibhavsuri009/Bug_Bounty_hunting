# SQLmap Saved-Request Parameter Test

- What it is: SQLmap can test a Burp-saved API request while preserving headers/body/auth.
- Where to look / how to identify it:
  - Save a known-good request, then run `sqlmap -r /home/hapihacker/burprequest1 -p password`; omit `-p` only when broad parameter testing is appropriate.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Automated findings require manual confirmation and can be noisy.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Parameterize queries and minimize DB privileges.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
