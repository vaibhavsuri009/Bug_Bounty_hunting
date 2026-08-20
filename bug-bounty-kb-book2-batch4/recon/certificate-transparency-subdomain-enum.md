# Certificate Transparency Subdomain Enumeration

- What it is: Public certificate records reveal hostnames that have received TLS certificates.
- Search `crt.sh` for the target's certificates and associated subdomains.
- Review historical entries, not just currently resolving names.
- A 404 on a discovered subdomain can be a clue that its backend/domain was retired.
- Wildcard certificates appear with `*` and do not enumerate every concrete host directly.
- Use certificate data as discovery input, then validate DNS and HTTP behavior separately.
- False positive: a certificate hostname may be expired, parked, or no longer owned.
- Edge case: certificates can contain unrelated SANs from shared infrastructure.
- Remediation: monitor certificate transparency and decommission stale DNS mappings.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
