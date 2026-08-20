# Search Index Permission Synchronization

- What it is: Separate search databases can leak stale or unauthorized data when permissions/deletions are not synchronized with the primary database.
- Where to look / how to identify it:
  - Map primary-store-to-search-index replication, deletion, and permission update flows.
- Exploitation / test pattern:
  - Use controlled records to verify that permission changes and deletions propagate promptly.
- Tools + exact CLI syntax (if mentioned):
  - Search/database test environment.
- Common false-positive / WAF / edge-case notes:
  - Expected indexing delay is not automatically a vulnerability unless it exposes data beyond policy.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Propagate authorization metadata, remove stale records, and enforce authorization at query time.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 21
