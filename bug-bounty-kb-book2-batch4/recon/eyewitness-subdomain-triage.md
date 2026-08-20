# EyeWitness Subdomain Visual Triage

- What it is: Screenshot automation helps prioritize large subdomain inventories.
- Enumerate in-scope subdomains first.
- Feed responsive hosts to EyeWitness to capture screenshots and common web ports.
- Prioritize staging/development panels, old CMSs, default pages, and unusual services.
- The book notes EyeWitness checks common web ports including 80, 443, 8080, and 8443.
- Treat screenshots as triage, then verify manually.
- False positive: an old-looking page is not itself vulnerable.
- Edge case: authentication/CDN interstitials can make screenshots misleading.
- Remediation note: remove obsolete internet-facing staging/admin systems.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 18
