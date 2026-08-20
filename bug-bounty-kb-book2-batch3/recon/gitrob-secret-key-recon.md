# Public Repository Secret Recon with Gitrob

- What it is: Repository reconnaissance searches connected public repos for sensitive filenames/keywords.
- The book describes Gitrob starting from a repository, person, or organization and spidering related repositories.
- Look for terms such as `password`, `secret`, and `database`.
- Validate whether exposed values are current before testing any downstream impact.
- High-value examples include framework signing keys such as Rails `secret_key_base`.
- Do not assume a committed secret is active merely because it is visible in history.
- False positive: examples, test fixtures, and revoked credentials are common.
- Edge case: old commits may still expose secrets even after the current branch is cleaned.
- Remediation: rotate exposed secrets and remove them from deployment/config history.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
- Validation: compare with an unmodified control request and record the exact response difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 12
