# GraphQL Capability Recon

- What it is: GraphQL can wrap existing APIs and offer field selection, arguments, aliases, fragments, variables, directives, operations, and mutations.
- Where to look / how to identify it:
  - Identify GraphQL endpoints and document supported operations before later authorization and injection testing.
- Exploitation / test pattern:
  - Capture representative queries and add object fields/arguments to the application map.
- Tools + exact CLI syntax (if mentioned):
  - DevTools Network/Response and GraphQL documentation if exposed.
- Common false-positive / WAF / edge-case notes:
  - Complex queries are normal; exposure becomes risky when authorization, depth, or field controls are weak.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Authorize every resolver/field and restrict query complexity and introspection appropriately.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
