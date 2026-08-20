# Open Redirect Google Dorks

- **What it is:** Uses indexed URLs to locate likely redirect parameters across a target domain.
- **Where to look:** Search engine results containing URL-valued query parameters.
- Start with the in-scope domain, then search for encoded `=http`, `=/`, and common redirect parameter names.

```text
inurl:%3Dhttp site:example.com
inurl:%3D%2F site:example.com
inurl:redir site:example.com
inurl:redirect site:example.com
inurl:returnurl site:example.com
inurl:relaystate site:example.com
inurl:forward site:example.com
inurl:dest site:example.com
inurl:next site:example.com
```

- Record discovered endpoints, then verify manually because indexed URLs may be stale.
- **False positives / edge cases:** Search results can expose out-of-scope hosts; validate program scope before testing.
- **Remediation:** Not applicable to search indexing itself; secure every redirect handler found.

## Source: Bug Bounty Bootcamp, Ch. 7
