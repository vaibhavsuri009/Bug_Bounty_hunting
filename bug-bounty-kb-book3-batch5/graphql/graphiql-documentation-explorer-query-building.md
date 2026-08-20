# GraphiQL Documentation Explorer Query Building

- What it is: The GraphiQL Documentation Explorer can be used to understand types, fields, and accepted arguments without guessing request syntax.
- Where to look / how to identify it:
  - Open Root Types, inspect `Query` or `Mutation`, then review the object fields that can be requested.
- Exploitation / test pattern:
  - Construct the smallest valid query first, then add only the fields needed for testing.
- Tools + exact CLI syntax (if mentioned):
  - `query { pastes(public: true) { title content public ipAddr pId } }`
- Common false-positive / WAF / edge-case notes:
  - A successful query only proves the field is exposed; it does not prove authorization is broken.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Expose only necessary fields and validate authorization per resolver and field.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
