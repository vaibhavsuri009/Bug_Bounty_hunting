# CNAME to Unregistered Domain Takeover

- What it is: A subdomain CNAME points to a separate registrable domain that has expired or was never registered.
- Enumerate CNAME targets that are ordinary domains rather than SaaS provider hostnames.
- If the subdomain returns a 404 or resolution anomaly, check the CNAME target's registration status.
- The book's Shopify Windsor example found the target domain available for registration.
- Confirm the DNS relationship before claiming anything.
- Use a benign proof only if the bounty rules allow domain registration.
- False positive: registrar search results can be stale or the registry may reserve the domain.
- Edge case: purchasing the domain can create real traffic impact, so minimize exposure.
- Remediation: remove CNAMEs before allowing referenced domains to expire.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
