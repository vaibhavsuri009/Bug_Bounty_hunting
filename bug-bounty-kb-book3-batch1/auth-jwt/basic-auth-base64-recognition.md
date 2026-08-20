# Basic Authentication Base64 Recognition

- What it is: HTTP Basic credentials are encoded, not encrypted, and can be trivially decoded if captured.
- Look for `Authorization: Basic ...` or Base64 strings representing `username:password`.
- The book demonstrates encoding and decoding from the Linux shell:
```bash
echo "username:password" | base64
echo "dXNlcm5hbWU6cGFzc3dvcmQK" | base64 -d
```
- Decode captured Basic values only within an authorized assessment.
- Test whether Basic auth is ever transmitted over plain HTTP.
- False positive: Base64-looking data may encode non-credential content.
- Edge case: TLS protects Basic credentials in transit but does not prevent credential reuse/brute force.
- Remediation: enforce TLS and prefer short-lived tokens/stronger authentication schemes.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 2
