# Authentication vs Authorization Map

- What it is: Authentication proves identity; authorization decides what resources and actions that identity may access.
- Where to look / how to identify it:
  - For each workflow, record both how the user authenticates and the authorization boundary protecting the requested resource.
- Exploitation / test pattern:
  - Separate auth failures from authorization failures when documenting findings.
- Tools + exact CLI syntax (if mentioned):
  - Request headers, tokens, cookies, role/permission observations.
- Common false-positive / WAF / edge-case notes:
  - A valid login does not imply correct authorization, and a denied resource does not imply authentication failed.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize authorization and perform server-side checks on every protected resource/action.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 3
