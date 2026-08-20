# Burp Sequencer Manual Token Analysis

- What it is: Sequencer measures token randomness and weak positions.
- Where to look / how to identify it:
  - Collect at least 100 controlled tokens; Sequencer → Manual Load → Analyze Now; inspect entropy and character-position analysis; focus on low-entropy positions.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Partial predictability does not automatically make the full token guessable.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Use CSPRNG-generated high-entropy tokens.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 8
