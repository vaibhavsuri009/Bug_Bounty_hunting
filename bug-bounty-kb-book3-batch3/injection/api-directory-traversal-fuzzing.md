# API Directory Traversal Fuzzing

- What it is: Traversal payloads attempt to escape an intended API/file path.
- Where to look / how to identify it:
  - Test path-like inputs using `..`, `../`, `..\`, `\..\`; start wide with a small set, then deep-fuzz responsive fields; use recon/error clues for target paths.
- Exploitation / test pattern:
  - Use controlled accounts/resources and start from a known-good request.
  - Change one relevant variable at a time and compare the server-side result with the clean baseline.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Normalization errors do not prove arbitrary file read; OS/decode behavior varies.
  - Confirm the actual server-side effect before reporting an anomaly.
- Remediation: Canonicalize paths and enforce a fixed allowed base directory.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 9
