# SSRF URL-Parameter Discovery

- What it is: A server fetches a URL/IP supplied by the user.
- Look for parameters named `url`, `uri`, `path`, `image`, `feed`, `webhook`, or remote import fields.
- Point the feature to an HTTP endpoint you control.
```text
?url=https://your-test-server.example/ssrf
```
- Confirm the request originates from the target infrastructure.
- Then determine whether the target returns the fetched response or is blind.
- False positive: the feature may intentionally fetch arbitrary external URLs and have no sensitive reach.
- Edge case: redirects, allowed schemes, ports, and response rendering determine impact.
- Remediation: strict destination allowlists plus network egress controls.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 10
