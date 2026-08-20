# SSRF Allowlist Bypass via Open Redirect

- A URL allowlist may be bypassed when an allowlisted host contains an open redirect.
- Supply the allowlisted redirect URL, with its redirect destination set to an internal address.
```http
POST /upload_profile_from_url
user_id=1234&url=https://pics.example.com/123?redirect=127.0.0.1
```
- The initial hostname passes the allowlist; the server then follows the redirect to the restricted destination.
- Verify whether the server follows 3XX responses before concluding the chain works.
- Test only redirects on domains already allowed by the target fetcher.
- Tools: Burp Repeater for redirect-chain testing.
- False-positive trap: secure fetchers revalidate every redirect hop or disable redirects entirely.
- Remediation: validate the resolved destination after every redirect and reject transitions to restricted networks.
## Source: Bug Bounty Bootcamp, Ch. 13
