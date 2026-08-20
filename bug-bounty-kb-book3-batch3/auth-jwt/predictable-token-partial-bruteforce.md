# Predictable Token Partial Brute Force

- What it is: Brute-force only the token characters Sequencer shows as low entropy.
- Where to look / how to identify it:
  - Create one attack position per weak character; constrain charsets from samples; use Intruder Cluster Bomb or Wfuzz multiple payload positions; validate candidates on a harmless authenticated endpoint.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Multiple candidates may map to the same controlled session.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use high-entropy tokens with proper invalidation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
