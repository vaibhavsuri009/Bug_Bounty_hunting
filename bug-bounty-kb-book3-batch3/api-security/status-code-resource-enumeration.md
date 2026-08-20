# Resource Enumeration by Status-Code Differences

- What it is: Different responses for existing vs nonexistent objects create a side channel.
- Where to look / how to identify it:
  - Compare clearly invalid identifiers with known-valid controlled values; stable `404` vs `401`/other differences can enumerate usernames/IDs/phones/emails.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Caches/gateways can create unstable codes; length/timing may be stronger.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Normalize unauthorized/nonexistent responses where practical.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 7
