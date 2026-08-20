# Wildcard Certificate Hash Pivot with Censys

- What it is: A wildcard certificate's unique hash can be searched across internet scan data to reveal hosts using it.
- Start with a wildcard certificate discovered through certificate transparency.
- Extract its certificate fingerprint/hash.
- Search Censys for systems presenting the same certificate.
- Use resulting hostnames as candidate subdomains/assets to validate.
- The technique helps when `crt.sh` shows only `*.example.com`.
- False positive: the same certificate may legitimately appear on shared proxies/CDNs.
- Edge case: renewed certificates change hashes and require re-pivoting.
- Remediation note: this is reconnaissance; asset owners should track certificate deployments and stale DNS.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 14
