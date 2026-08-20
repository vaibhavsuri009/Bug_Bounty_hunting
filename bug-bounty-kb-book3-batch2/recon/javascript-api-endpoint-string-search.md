# JavaScript API Endpoint String Search

- What it is: Frontend JavaScript often contains route constants for login, signup, reset, vehicle, order, and other API functions.
- Open DevTools Network and refresh the target.
- Send a JavaScript bundle to Sources.
- Search the bundle for `API`, `/api/`, auth verbs, or feature names.
- Record discovered endpoints and map each constant to its likely business function.
- Trigger the related UI action and capture the real request in Burp to validate the endpoint.
- False positive: bundles may contain dead code or routes for disabled features.
- Edge case: minified/hashed filenames change between builds.
- Remediation: treat client-side route discovery as expected and enforce backend security independently.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
- Validation: confirm the finding manually against a clean baseline before treating it as exploitable.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 6
