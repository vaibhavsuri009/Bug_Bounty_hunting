# Public Record Secret Discovery

- What it is: Search engines, archived repositories, social posts, and public caches can retain secrets or infrastructure references after removal from the live application.
- Where to look / how to identify it:
  - Search for exposed SSH keys, cloud/service keys, internal URLs, usernames, emails, and accidentally public code belonging to the authorized target.
- Exploitation / test pattern:
  - Record provenance and verify whether any credential is already revoked before reporting.
- Tools + exact CLI syntax (if mentioned):
  - Search engines, archives, public repositories, social media.
- Common false-positive / WAF / edge-case notes:
  - Old or fake values may appear; validate safely and avoid accessing unrelated private systems.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use secret scanning, rapid key rotation, repository controls, and removal from public caches when possible.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 4
