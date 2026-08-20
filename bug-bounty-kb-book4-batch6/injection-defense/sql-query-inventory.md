# SQL Query Inventory

- What it is: Defending SQL injection starts with locating every SQL/DSL query surface in the server codebase.
- Where to look / how to identify it:
  - Search imports, query methods, ORM/DSL usage, analytics modules, and every database adapter.
- Exploitation / test pattern:
  - Create a complete inventory before reviewing for parameterization and user-input flow.
- Tools + exact CLI syntax (if mentioned):
  - Source search for database imports and `.query`-style calls.
- Common false-positive / WAF / edge-case notes:
  - Multiple databases/adapters can use very different syntax.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Maintain shared secure data-access libraries and scan all database implementations.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 31
