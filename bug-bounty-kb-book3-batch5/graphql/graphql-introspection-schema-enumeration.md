# GraphQL Introspection Schema Enumeration

- What it is: GraphQL introspection can disclose the API schema, including query, mutation, subscription, types, fields, and arguments.
- Where to look / how to identify it:
  - Look for GraphiQL/Playground documentation or send an introspection query on an authorized target.
- Exploitation / test pattern:
  - Use the returned schema to map callable operations and build a structured test collection.
- Tools + exact CLI syntax (if mentioned):
  - `query IntrospectionQuery { __schema { queryType { name } mutationType { name } types { ...FullType } } }`
- Common false-positive / WAF / edge-case notes:
  - Introspection is useful functionality and is not automatically a vulnerability; severity depends on what sensitive operations become exposed.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Disable or restrict introspection in production when not required and enforce authorization on every resolver.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
