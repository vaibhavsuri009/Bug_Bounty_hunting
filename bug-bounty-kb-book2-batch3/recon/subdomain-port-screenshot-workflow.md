# Subdomain + Port + Screenshot Recon Workflow

- What it is: Large scopes are reduced to interesting targets through automated asset discovery and visual triage.
- The book's workflow uses Sublist3r, Aquatone, Nmap, then EyeWitness.
- Enumerate subdomains first.
- Scan authorized hosts for exposed ports/services.
- Use screenshots to quickly identify old admin panels, unfamiliar CMSs, and unusual services.
- Prioritize outdated/open-source applications for deeper review.
- Check program scope before scanning broad address ranges.
- False positive: an old-looking interface is not itself a vulnerability.
- Remediation note: remove unnecessary services and keep internet-facing software patched.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
