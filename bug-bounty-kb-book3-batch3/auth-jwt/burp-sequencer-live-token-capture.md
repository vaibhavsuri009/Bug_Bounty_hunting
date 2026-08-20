# Burp Sequencer Live Token Capture

- What it is: Sequencer can repeatedly trigger token generation and analyze results.
- Where to look / how to identify it:
  - Intercept token-generation request; send to Sequencer Live Capture; configure token location; Start Live Capture; optionally Auto Analyze.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Large captures may hit rate limits or create server-side state.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use strong entropy and correct rotation/invalidation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
