# Recon Note Relationship Preservation

- What it is: Recon notes are most useful when they preserve hierarchy and relationships rather than only storing flat lists of URLs.
- Where to look / how to identify it:
  - Link endpoints to features, authentication requirements, user roles, integrations, and observed data models.
- Exploitation / test pattern:
  - Update notes continuously as new relationships are discovered.
- Tools + exact CLI syntax (if mentioned):
  - JSON-like notes, Notion, XMind, or another hierarchical system.
- Common false-positive / WAF / edge-case notes:
  - Overly detailed notes can become hard to traverse; keep a consistent compact schema.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Organizations should maintain equivalent architecture and data-flow documentation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 2
