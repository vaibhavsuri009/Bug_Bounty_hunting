# JavaScript Exposed API Key

- What it is: Frontend JavaScript may contain reusable API credentials, keys, endpoints, or Basic-auth material.
- Where to look / how to identify it:
  - Search source files for `api`, `key`, `secret`, `Authorization`, and encoded credential-looking strings.
- Exploitation / test pattern:
  - Decode reversible encodings such as base64 and validate only with low-impact, authorized requests.
- Tools + exact CLI syntax (if mentioned):
  - `echo 'BASE64_VALUE' | base64 -d`
- Common false-positive / WAF / edge-case notes:
  - Base64 is encoding, not encryption; a key can still be scoped or non-sensitive.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Never ship privileged credentials to client-side code; rotate exposed secrets and use server-side mediation.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 15
