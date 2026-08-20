# Dangling CNAME Subdomain Takeover

- What it is: A target subdomain still CNAMEs to a third-party resource that no longer exists and can be claimed.
- Enumerate subdomains and resolve their CNAME chains.
- Visit the target and note provider-specific "not found / unconfigured" responses.
- Confirm the referenced third-party hostname/resource is unclaimed.
- Services mentioned in the book include Heroku, Zendesk, GitHub, S3, SendGrid, and Fastly.
- Use only a nonintrusive proof if program rules permit claiming the resource.
- False positive: a provider error page does not guarantee the custom domain can be claimed.
- Edge case: modern providers increasingly require DNS ownership verification.
- Remediation: remove DNS records before deleting third-party resources.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
