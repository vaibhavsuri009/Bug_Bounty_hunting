# SSRF Regex Allowlist Bypass

- Weak regex allowlists may only check whether an approved hostname appears somewhere in the URL.
- Test parser ambiguity by moving the allowlisted text into userinfo or path components.
```text
https://pics.example.com@127.0.0.1
https://127.0.0.1/pics.example.com
```
- In the first URL, `pics.example.com` is userinfo and `127.0.0.1` is the hostname.
- In the second, the approved hostname is only part of the path.
- Compare what the validator accepts with where the HTTP client actually connects.
- This works only against incorrectly constructed validation logic; a correct parser-aware allowlist will reject it.
- Tools: Burp Repeater for controlled mutation.
- Remediation: parse URLs with a standard parser and compare the canonical hostname against an exact allowlist.
## Source: Bug Bounty Bootcamp, Ch. 13
