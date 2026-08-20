# GraphQL Request Reverse Engineering

- What it is: GraphQL requests often look identical at the URL level because behavior is defined by the POST body.
- Where to look / how to identify it:
  - Capture application traffic and review each GraphQL request body for operation names, fields, variables, and arguments.
- Exploitation / test pattern:
  - Rename and group captured requests by operation so a reusable collection can be built for later testing.
- Tools + exact CLI syntax (if mentioned):
  - Postman capture/proxy plus Burp Proxy/Repeater.
- Common false-positive / WAF / edge-case notes:
  - Do not assume two `/graphql` requests do the same thing; inspect the operation body.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Document and restrict GraphQL operations; minimize unnecessary fields and mutations.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 14
