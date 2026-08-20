# XXE Password-Hash Escalation Risk

- What it is: If a vulnerable parser can read restricted authentication files, exposed password hashes could theoretically be cracked offline.
- Where to look / how to identify it:
  - Document whether parser privileges would allow access to credential stores without extracting real user hashes on a live target.
- Exploitation / test pattern:
  - Use lab-only synthetic hashes if demonstrating the risk technically.
- Tools + exact CLI syntax (if mentioned):
  - Book mentions `unshadow`, John the Ripper, and Hashcat for lab workflows.
- Common false-positive / WAF / edge-case notes:
  - Offline cracking speed depends heavily on hash algorithm, salt, and password quality.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Protect credential files with OS permissions, modern password hashing, and low-privilege parser execution.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 12
