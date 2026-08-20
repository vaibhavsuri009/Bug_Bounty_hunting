# Subdomain Takeover Enumeration with KnockPy

- What it is: KnockPy enumerates subdomains and checks responses for takeover-related service errors.
- Use it against domains explicitly in scope.
- Feed its built-in subdomain list or a custom wordlist.
- Review CNAMEs and provider-specific errors rather than trusting automation blindly.
- Supplement candidate names with SecLists subdomain wordlists.
- Recheck candidates over time because DNS/service state changes.
- False positive: automated signatures can match an error page even when registration is protected.
- Edge case: takeover feasibility may depend on account tier, TLS, or ownership-verification requirements.
- Remediation: continuously inventory DNS and retire stale records.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
