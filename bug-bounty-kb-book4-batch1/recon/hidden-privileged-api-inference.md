# Hidden Privileged API Inference

- What it is: Functionality available to internal staff implies backend operations may exist even when the public UI does not expose them.
- Where to look / how to identify it:
  - Look for workflows such as account creation, account modification, moderation, support actions, and administrative updates.
- Exploitation / test pattern:
  - Map the public workflow and infer related CRUD operations that privileged roles would require; search only within authorized scope.
- Tools + exact CLI syntax (if mentioned):
  - DevTools/HTTP history plus structured notes.
- Common false-positive / WAF / edge-case notes:
  - An inferred endpoint is not evidence that it exists or is accessible.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Inventory administrative APIs and require explicit server-side authorization on every privileged operation.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 2
