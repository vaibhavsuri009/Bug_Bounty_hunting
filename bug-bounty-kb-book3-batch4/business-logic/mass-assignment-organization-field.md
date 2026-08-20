# Mass Assignment into Organization/Tenant

- What it is: An unprotected organization/tenant field can let a user assign their account into another group.
- Where to look / how to identify it:
  - Identify org/company/group IDs from docs or controlled accounts; add or modify the organization property in a normal create/update request; verify resulting access with test tenants.
- Exploitation / test pattern:
  - Start from a known-good request using only controlled accounts/resources.
  - Change one relevant field at a time and compare status, body, timing, and actual server-side effect.
- Tools + exact CLI syntax (if mentioned):
  - Reusable commands from the book are included above when applicable.
- Common false-positive / WAF / edge-case notes:
  - Some org fields are display metadata only.
  - Confirm impact manually before reporting or chaining the result.
- Remediation: Authorize organization membership changes and keep tenant IDs server-managed.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 11
