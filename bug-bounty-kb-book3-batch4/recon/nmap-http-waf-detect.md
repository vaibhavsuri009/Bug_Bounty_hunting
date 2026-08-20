# Nmap HTTP WAF Detection

- What it is: Nmap's HTTP WAF detection script can identify some web application firewalls.
- Where to look / how to identify it:
  - Book syntax: `nmap -p 80 --script http-waf-detect http://hapihacker.com`; confirm detected products manually from responses.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Detection scripts can miss or misidentify WAFs.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: No direct remediation; validate edge security configuration.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 13
