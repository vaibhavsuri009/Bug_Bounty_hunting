# API Passive Recon Workflow

- What it is: Passive recon maps an API attack surface without directly interacting with target systems.
- Collect endpoints, credentials/secrets, version information, documentation, and business-purpose clues.
- Start broad using search engines, API directories, DNS mapping, and Amass.
- Then adapt searches using names, domains, products, technologies, and findings from phase one.
- Search public repositories/pastes for secrets and endpoint references.
- Document every useful lead and maintain a follow-up task list.
- False positive: public data can be stale or refer to third parties.
- Edge case: leaked secrets should be reported promptly rather than aggressively tested.
- Remediation: continuously monitor public exposure, repositories, and documentation.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
