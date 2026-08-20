# Least Authority for Interpreter Modules

- What it is: A compromised low-privilege module causes less damage than a CLI/database helper running with broad system permissions.
- Where to look / how to identify it:
  - Review filesystem, database, network, logging, and OS privileges for each module/service identity.
- Exploitation / test pattern:
  - Remove permissions unrelated to the module's exact job.
- Tools + exact CLI syntax (if mentioned):
  - OS/IAM/database role configuration.
- Common false-positive / WAF / edge-case notes:
  - Least privilege limits blast radius but cannot prevent the initial injection.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Use separate service identities and narrowly scoped permissions.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 31
