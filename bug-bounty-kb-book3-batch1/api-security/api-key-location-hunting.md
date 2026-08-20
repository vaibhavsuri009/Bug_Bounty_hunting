# API Key Location Hunting

- What it is: API keys may appear in query strings, headers, bodies, cookies, frontend files, or public repositories.
- Inspect every request location and application source for key-like high-entropy strings.
- Common patterns shown include `?apikey=...`, custom secret headers, and `Cookie: API-Key=...`.
- Search JavaScript and public code repositories for hardcoded keys.
- If a key is found, determine its associated role and scope using only authorized test actions.
- False positive: sample/revoked keys are common in documentation.
- Edge case: keys in URLs can leak through logs, browser history, and referrers.
- Remediation: keep keys out of URLs/source code, scope them minimally, and rotate exposed values.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 2
