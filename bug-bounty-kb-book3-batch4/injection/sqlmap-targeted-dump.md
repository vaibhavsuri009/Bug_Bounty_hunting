# SQLmap Targeted Data Dump

- What it is: A confirmed SQLi can be validated by retrieving only a minimal authorized test dataset.
- Where to look / how to identify it:
  - Book syntax: `sqlmap -r /home/hapihacker/burprequest1 -p vuln-param --dump -T users -C password -D helpdesk`; use only lab/test data rather than broad production dumping.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - `--dump-all` is unnecessarily invasive for most bounty validation.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Fix SQLi with parameterized queries and rotate exposed credentials.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
