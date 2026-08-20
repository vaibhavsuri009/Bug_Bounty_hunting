# API Information Disclosure Response Review

- What it is: API responses expose sensitive data or implementation details to users who do not need them.
- Review headers, JSON/XML bodies, verbose errors, documentation, and public API resources.
- Test known endpoints with both valid and invalid controlled identifiers.
- Compare messages for username/account enumeration clues.
- The book gives `/wp-json/wp/v2/users` as an example endpoint that can reveal WordPress usernames.
- Treat disclosed software versions, user IDs, logs, and keys as pivots for deeper testing.
- False positive: publicly documented/profile data may be intentionally exposed.
- Edge case: one sensitive field can be buried inside an otherwise legitimate response.
- Remediation: minimize responses and return uniform errors without sensitive internals.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
- Validation: compare modified behavior against a clean baseline and verify the server-side effect.
## Source: Hacking APIs — Breaking Web Application Programming Interfaces, Ch. 3
