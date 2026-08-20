# OAuth Forgotten Whitelisted Domain Takeover

- What it is: A trusted OAuth application's redirect domain expires or becomes claimable while remaining whitelisted/preauthorized.
- Inventory redirect domains used by official or preauthorized OAuth clients.
- Check whether any referenced domain is no longer owned by the target.
- If rules permit, prove control nonintrusively without collecting third-party tokens.
- The Facebook example involved an old official app whose redirect domain could be registered.
- Preauthorized apps are especially dangerous because users may not see a consent prompt.
- False positive: a dead domain may no longer be accepted by the authorization server.
- Edge case: the OAuth client ID may retain broad historical scopes.
- Remediation: continuously audit redirect URIs and decommission OAuth clients with their dependent domains.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 17
