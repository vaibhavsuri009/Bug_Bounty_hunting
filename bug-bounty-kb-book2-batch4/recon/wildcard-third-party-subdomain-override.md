# Wildcard Third-Party Subdomain Override

- What it is: A SaaS platform lets a wildcard custom-domain claim override a more specific hostname already assigned to another customer.
- If the exact subdomain is already claimed, review whether the provider accepts `*.example.com`.
- Test only on your own controlled domain first to understand precedence rules.
- The Legal Robot example found a wildcard claim overriding `api.example.com`.
- Use a harmless static page/comment for proof if target testing is explicitly allowed.
- False positive: modern routing commonly gives exact hostnames precedence over wildcard routes.
- Edge case: TLS/domain verification may prevent wildcard registration even when routing logic is weak.
- Remediation: providers must verify wildcard ownership and prioritize exact validated bindings.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
