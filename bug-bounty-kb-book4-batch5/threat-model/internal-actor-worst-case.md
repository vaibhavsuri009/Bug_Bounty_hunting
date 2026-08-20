# Internal Actor Worst-Case Modeling

- What it is: Admins, internal users, privileged scripts, and service tokens can become threat actors through compromise, bugs, or malicious intent.
- Where to look / how to identify it:
  - Identify high-privilege identities and what would happen if each were fully compromised.
- Exploitation / test pattern:
  - Model worst-case actions rather than assuming internal actors use functionality correctly.
- Tools + exact CLI syntax (if mentioned):
  - Threat model + IAM review.
- Common false-positive / WAF / edge-case notes:
  - Not every privileged identity requires identical controls; scope by actual function.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Apply least privilege, separation of duties, immutable logging, and short-lived credentials.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
