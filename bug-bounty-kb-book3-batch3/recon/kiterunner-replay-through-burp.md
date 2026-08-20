# Replay Kiterunner Results Through Burp

- What it is: Proxy Kiterunner replay into Burp for manual verification.
- Where to look / how to identify it:
  - `kr kb replay -w ~/api/wordlists/data/kiterunner/routes-large.kite --proxy=http://127.0.0.1:8080 "RESULT_LINE"`; send to Repeater and change one field at a time.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Replay can fail after token/state changes.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Apply equal controls to undocumented endpoints.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
