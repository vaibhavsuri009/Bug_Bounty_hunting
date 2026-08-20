# GraphQL Compute Limits

- What it is: GraphQL circular or deeply nested queries can consume excessive server resources even when conventional request rate limits are present.
- Where to look / how to identify it:
  - Threat-model GraphQL depth, cycles, resolver fan-out, aliases, and expensive nested operations.
- Exploitation / test pattern:
  - Use a local/staging query-cost model rather than load-testing production.
- Tools + exact CLI syntax (if mentioned):
  - GraphQL complexity/depth controls.
- Common false-positive / WAF / edge-case notes:
  - Simple query count limits do not capture expensive single queries.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Set depth/complexity/time budgets and terminate requests that exceed them.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 24
