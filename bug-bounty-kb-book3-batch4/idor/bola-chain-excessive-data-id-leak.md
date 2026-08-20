# Chain Excessive Data Exposure into BOLA

- What it is: An excessive-data endpoint can leak object IDs that make otherwise unguessable BOLA exploitation practical.
- Where to look / how to identify it:
  - Search overexposed responses for GUIDs/UUIDs such as `vehicleid`; substitute the leaked ID into a known BOLA-prone resource request using a controlled alternate token.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Leaked IDs alone are not BOLA; the second endpoint must fail authorization.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Minimize identifier exposure and enforce authorization independently.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 10
