# File IDOR via Direct Filename Reference

- What it is: IDOR occurs when a user-supplied path or identifier directly selects a server-side object without ownership validation.
- Where to look / how to identify it:
  - Look for file IDs, filenames, numeric IDs, UUIDs, and document references in paths, queries, or request bodies.
- Exploitation / test pattern:
  - Use two controlled accounts/files and swap only the identifier.
- Tools + exact CLI syntax (if mentioned):
  - Browser/Proxy request editing.
- Common false-positive / WAF / edge-case notes:
  - Guessability is not the vulnerability; unauthorized access is.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Authorize each requested object against the current user before retrieval.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 15
