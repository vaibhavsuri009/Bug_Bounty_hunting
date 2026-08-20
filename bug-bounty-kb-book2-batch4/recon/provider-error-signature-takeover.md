# Provider Error-Signature Takeover Testing

- What it is: Third-party platforms often expose recognizable errors when a custom domain points to an unconfigured service.
- Record the exact error text and identify the provider.
- Read the provider's custom-domain documentation before attempting a claim.
- The book cites Fastly's "unknown domain ... not added to a service" style error as a clue.
- Confirm target ownership of ambiguous domains using TLS certificate/registration information.
- Validate whether the subdomain is actually receiving production traffic before rating impact.
- False positive: an error page can exist while provider-side domain verification blocks takeover.
- Edge case: legacy app versions may be the only clients still using the host.
- Remediation: enforce ownership verification and remove unused DNS records.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
