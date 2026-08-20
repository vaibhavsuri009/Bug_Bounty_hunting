# HTTP OPTIONS Method Enumeration

- What it is: Use `OPTIONS` to learn which HTTP methods a server advertises for an endpoint.
- Where to look: API routes and sensitive endpoints where alternate request methods may expose different behavior.
- Send an `OPTIONS` request to the endpoint under test.
- Review the response for accepted methods such as `GET`, `POST`, `PUT`, `DELETE`, or `OPTIONS`.
- Compare advertised methods with the methods the normal UI actually uses.
- Test authorized methods separately because method availability does not prove authorization is enforced correctly.
- Note: The book states `OPTIONS` does not necessarily indicate support for `HEAD` or `TRACE`.
- Edge case: Browsers may automatically issue preflight `OPTIONS` requests for some cross-origin requests.
- Repeat the check on nearby API versions or alternate routes if the application exposes them.
- Record discrepancies where one route exposes a method that its peer does not.
- False-positive trap: An `Allow`/CORS response is reconnaissance only; a security issue requires unsafe behavior or access-control impact.
- Remediation: Expose only required methods and enforce identical authorization controls per method.
## Source: Real-World Bug Hunting — A Field Guide to Web Hacking, Ch. 1
