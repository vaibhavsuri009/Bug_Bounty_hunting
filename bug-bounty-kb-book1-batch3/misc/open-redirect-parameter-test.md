# Parameter-Based Open Redirect Test

- **What it is:** Confirms whether a redirect parameter accepts an external attacker-controlled destination.
- **Where to look:** Any endpoint that redirects after login, logout, registration, or another workflow step.
- Replace the normal destination with a hostname you control or a harmless external test host.
- Complete any required workflow action before judging the result.

```text
https://example.com/login?next=https://attacker.example/
https://example.com/logout?redirect=https://attacker.example/
```

- Confirm the browser ultimately navigates off the trusted origin.
- Capture the `3xx` response and `Location` header when present.
- **False positives / edge cases:** Client-side redirects may not return `3xx`; inspect JavaScript and final browser location.
- **Remediation:** Reject untrusted origins and prefer relative internal paths.

## Source: Bug Bounty Bootcamp, Ch. 7
