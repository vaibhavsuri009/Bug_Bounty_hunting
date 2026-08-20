# Wfuzz Command Separator + Command Matrix

- What it is: Two Wfuzz payload sets can test separator/command combinations systematically.
- Where to look / how to identify it:
  - Book pattern: `wfuzz -z file,wordlists/commandsep.txt -z file,wordlists/os-cmds.txt http://vulnerableAPI.com/api/users/query?=WFUZZWFUZ2Z`; review anomalous status/length responses.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - High request volume can trigger controls; keep payloads harmless in authorized testing.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Remove shell concatenation and enforce strict command argument handling.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 12
