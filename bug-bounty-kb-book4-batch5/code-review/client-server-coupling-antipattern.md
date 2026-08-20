# Client/Server Coupling Anti-Pattern

- What it is: Tightly mixing rendering, authentication, database logic, and client data formats increases the number of security contexts each module must handle.
- Where to look / how to identify it:
  - Look for server code parsing or emitting executable HTML while simultaneously performing authentication or business logic.
- Exploitation / test pattern:
  - Map whether APIs use a clear predefined data format independent of client rendering.
- Tools + exact CLI syntax (if mentioned):
  - Architecture/source review.
- Common false-positive / WAF / edge-case notes:
  - Server-side rendering is not inherently insecure; risk comes from unstructured coupling and mixed trust boundaries.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Separate concerns, use explicit API schemas, and keep authorization/data logic independent of presentation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 25
