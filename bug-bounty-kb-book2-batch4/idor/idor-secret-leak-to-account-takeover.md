# IDOR Secret Leak to Account Takeover

- What it is: Broken object authorization leaks API keys/secrets that are later reusable for authentication.
- First confirm an endpoint returns another controlled account's secret material when its organization/object ID is changed.
- Identify where each leaked secret is consumed elsewhere in the platform.
- Test whether a secret acts as a login/authorization code only with your own accounts.
- The Mopub example escalated from `api_key`/`build_secret` disclosure to account access.
- Trace identifier leakage separately; the object ID itself may come from public share URLs/search results.
- False positive: a returned secret may be scoped, expired, or non-authenticating.
- Edge case: impact often depends on chaining multiple weak controls.
- Remediation: enforce object authorization and rotate exposed secrets.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
- Validation: compare the modified request/action with a clean control and record the exact server-side difference.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 16
