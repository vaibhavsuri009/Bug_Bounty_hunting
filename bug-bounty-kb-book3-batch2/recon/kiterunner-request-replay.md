# Kiterunner Request Replay

- What it is: Replay reconstructs the exact request behind an interesting Kiterunner discovery result.
- Copy the complete Kiterunner result line.
- Replay it with the same route wordlist:
```bash
kr kb replay "RESULT_LINE" -w ~/api/wordlists/data/kiterunner/routes-large.kite
```
- Inspect the full HTTP response to understand why the route was flagged.
- Pivot validated endpoints into Postman or Burp for manual analysis.
- False positive: an interesting status/length combination may still be a generic error.
- Edge case: replay may differ if tokens, cookies, or server state changed.
- Remediation note: consistent auth controls should apply to discovered and undocumented routes alike.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
