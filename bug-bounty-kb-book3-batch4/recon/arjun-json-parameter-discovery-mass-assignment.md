# Arjun JSON Parameter Discovery for Mass Assignment

- What it is: Arjun can discover accepted JSON parameter names by response deviations.
- Where to look / how to identify it:
  - Book syntax: `arjun --headers "Content-Type: application/json" -u http://vulnhost.com/api/register -m JSON --include='{$arjun$}'`; add authorization headers when required; use `--stable` if rate limiting/instability interferes.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Detected parameters still need manual impact validation.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Reject unknown fields and expose only documented writable parameters.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
