# API Version and Development-Path Enumeration

- What it is: Retired or development API versions may remain reachable with weaker controls.
- Review documentation, changelogs, repositories, and endpoint naming conventions.
- Test version patterns such as `/v1/`, `/v2/`, `/v3/`.
- Test development labels such as `/alpha/`, `/beta/`, `/test/`, `/uat/`, and `/demo/`.
- Compare old versions with the current API for authentication, data exposure, mass assignment, and rate limiting.
- Use fuzzing/guessing when documentation hints at older paths.
- False positive: an old path may simply redirect to the current implementation.
- Edge case: retired versions may be intentionally supported for legacy clients.
- Remediation: inventory, disable, or fully secure all deployed API versions/environments.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
