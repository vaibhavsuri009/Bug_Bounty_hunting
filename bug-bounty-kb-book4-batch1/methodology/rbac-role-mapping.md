# RBAC Role Mapping During Recon

- What it is: Modern applications commonly expose different functionality to customers, moderators, staff, administrators, and other roles.
- Where to look / how to identify it:
  - Identify visible and inferred roles, then map which features and API operations each role should legitimately access.
- Exploitation / test pattern:
  - Use multiple authorized test accounts at different roles to compare menus, requests, and backend functionality.
- Tools + exact CLI syntax (if mentioned):
  - Browser DevTools Network tab or an intercepting proxy can record role-specific requests.
- Common false-positive / WAF / edge-case notes:
  - UI differences are only clues; server-side authorization must be evaluated separately.
  - Keep testing limited to systems, accounts, and data explicitly authorized for the engagement.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Centralize authorization policy and document permissions per role and resource.
## Source: Web Application Security, 2nd Edition — Andrew Hoffman, Ch. 2
