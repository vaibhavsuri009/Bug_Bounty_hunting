# Open Redirect Security Impact Chaining

- **What it is:** Uses an open redirect as a trusted-origin hop inside a larger exploit chain.
- **Where to look:** Systems that allowlist target-owned URLs for SSRF, OAuth callbacks, token-bearing links, or navigation.
- Test whether an allowlisted target URL can redirect a downstream request to another origin.
- Also inspect whether sensitive values appear in the original URL and could leak through redirect/referrer behavior.

```text
https://example.com/?next=https://attacker.example/
```

- Treat phishing-only impact as lower confidence unless the program explicitly accepts it.
- Higher-value chains include allowlist bypasses and trusted redirect hops in other vulnerabilities.
- **False positives / edge cases:** Downstream clients may refuse redirects or strip sensitive headers/tokens.
- **Remediation:** Do not treat redirectable URLs as trusted endpoints; validate final destinations after redirects.

## Source: Bug Bounty Bootcamp, Ch. 7
