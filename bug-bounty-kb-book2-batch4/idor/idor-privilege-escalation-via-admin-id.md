# IDOR Privilege Escalation via Account/Administration ID

- What it is: A low-privileged user can submit another account's identifier to create a high-privilege resource.
- Build two controlled tenants/businesses with different permission levels.
- Capture a privileged resource-creation request from the tenant you own.
- Replay as the restricted user after replacing the tenant/account ID with the target controlled tenant's ID.
- Verify whether the created app/resource receives permissions the restricted user lacks.
- The Moneybird example used `administration_id`.
- False positive: UI visibility of the resource does not prove it has elevated API capabilities.
- Edge case: identifiers can be long/random but still leaked to members.
- Remediation: authorize the requested tenant ID and requested scopes server-side.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
