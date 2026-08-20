# Blind RCE Out-of-Band Confirmation

- **What it is:** Execution is confirmed by making the target initiate an observable outbound interaction.
- **Where to look:** Blind code/command injection where neither output nor reliable timing differences are available.
- **Test / exploitation:**
  - Set up a callback endpoint or listener you control.
  - Inject a harmless command that causes a DNS/HTTP/network interaction to your listener.
  - Correlate the received request with a unique payload marker.
  - Repeat once to confirm causality.
  - Do not escalate to an interactive shell unless the program explicitly permits it.
- **False positives / edge cases:**
  - Unrelated internet scanners can hit public listeners; use unique per-test identifiers.
- **Remediation:** Remove unsafe code execution and restrict unnecessary outbound connectivity.

## Source: Bug Bounty Bootcamp — The Guide to Finding and Reporting Web Vulnerabilities, Ch. 18
