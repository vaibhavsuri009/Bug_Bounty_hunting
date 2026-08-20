# API Documentation Attack-Surface Mapping

- What it is: API contracts often disclose endpoints, parameters, authentication requirements, roles, and privileged actions.
- Collect public or client-provided API documentation/specifications.
- Extract every endpoint, HTTP method, path variable, body parameter, and required privilege.
- Flag admin-only and destructive operations for authorization testing.
- Note optional/undocumented-looking parameters and alternate API versions.
- OpenAPI/Swagger and RAML specifications can be imported into API clients for systematic testing.
- False positive: documentation can be stale and describe retired functionality.
- Edge case: examples may contain placeholder credentials or IDs that are not live.
- Remediation: keep documentation accurate and avoid publishing unnecessary internal/admin details.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 2
